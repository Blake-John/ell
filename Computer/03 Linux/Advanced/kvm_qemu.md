对于 Arch 用户而言，一台 Windows 虚拟机显然是必不可少的，特别是具有 GPU 直连的虚拟机。使用 kvm/qemu 来创建 Windows 虚拟机能够做到占用资源少，启动速度快，且不卡顿。

# 01 Requirement

## 1.0 VMX

我们首先需要确认 CPU 是否支持虚拟化 :

```bash
grep -E 'vmx|svm' /proc/cpuinfo
```

如果有输出，则代表支持，若没有输出则应该在 BIOS 中启动虚拟化服务。

## 1.1 IOMMU

然后我们需要检查 `iommu` 内核是否启动，能否正常使用虚拟化 : 

```bash
sudo dmesg | grep -e "DMAR: IOMMU" 
```

若结果为 `DMAR: IOMMU enabled` 则证明可以正常使用虚拟化。如果没有，则应该在 `grub.cfg` 中追加驱动内核的选项 :

```bash
# /usr/default/grub
GRUB_CMDLINE_LINUX_DEFAULT="... intel_iommu=on iommu=pt"
# AMD 则改成 amd_iommu=on
```

然后重新生成启动配置，并重启电脑 :

```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
reboot
```

然后，我们可以回到第一步重新检查。

## 1.2 Packages

接下来，我们安装需要的软件与库 :

```bash
sudo pacman -S qemu-full virt-manager libvirt
```

- `qemu-full` - 使用 kvm/qemu 作为我们的虚拟机
- `virt-manager` - 通过可视化的方式创建虚拟机
- `libvirt` - 使用 `virt-manager` 创建虚拟机的依赖

安装好依赖后，我们需要启动服务，并将用户加入目标组中 :

```bash
sudo systemctl enable --now libvirtd
sudo usermod $USER -aG libvirt kvm
reboot
```

重启后，我们检查自己是否在 `libvirt` 以及 `kvm` 组中 :

```bash
groups
```

若输出包含，则存在。

## 1.3 VFIO

为了让虚拟机能够使用显卡，我们需要将 GPU 绑定到 VFIO 上。首先查看显卡设备和音频设备的 ID :

```bash
lspci -nn | grep -i nvidia
```

其输出如下，其中每个设备后的 8 位 ID 就是设备的特殊标识 :

```bash
01:00.0 VGA compatible controller [0300]: NVIDIA Corporation AD107M [GeForce RTX 4060 Max-Q / Mobile] [10de:28a0] (rev a1)
01:00.1 Audio device [0403]: NVIDIA Corporation AD107 High Definition Audio Controller [10de:22be] (rev a1)
```

然后，我们将 VGA 和 Audio 设备绑定到 VFIO 上，在 `/etc/modprobe.d/vfio.conf` 中写入 :

```bash
options vfio-pci ids=10de:28a0,10de:22be
softdep nvidia pre: vfio-pci
```

然后，我们重新编译启动引导项 :

```bash
sudo mkinitcpio -P
reboot
```

重启后检查设备是否成功绑定到 VFIO 上 :

```bash
lspci -nnk -d 10de:28a0
lspci -nnk -d 10de:22be
```

其输出应为如下 :

```bash
01:00.0 VGA compatible controller [0300]: NVIDIA Corporation AD107M [GeForce RTX 4060 Max-Q / Mobile] [10de:28a0] (rev a1)
	Subsystem: CLEVO/KAPOK Computer Device [1558:25a1]
	Kernel driver in use: vfio-pci
	Kernel modules: nouveau, nvidia_drm, nvidia
01:00.1 Audio device [0403]: NVIDIA Corporation AD107 High Definition Audio Controller [10de:22be] (rev a1)
	Subsystem: NVIDIA Corporation Device [10de:0000]
	Kernel driver in use: vfio-pci
	Kernel modules: snd_hda_intel
```

若 `Kernel driver in use` 显示为 `vfio-pci` 则证明绑定成功。

> [!important] 
> 在将 GPU 绑定到 VFIO 上之后，宿主机的 GPU 就不能再被使用， `nvidia-smi` 命令会提示找不到设备。如果我们希望将 GPU 将会给宿主机，只需要将 `/etc/modprobe.d/vfio.conf` 注释掉，然后重新编译启动项并重启即可

## 1.4 Network

为了能够让虚拟机正常使用网络，我们选择使用默认的网络配置 `nat` 为虚拟机提供网络，因此我们需要开启默认网络配置 :

```bash
sudo virsh net-autostart default
sudo virsh net-start default
sudo virsh net-list --all
```

若输出结果如下，则证明网络已经启动 :

```bash
 Name      State    Autostart   Persistent
--------------------------------------------
 default   active   yes         yes
```

> [!tip] 
> 如果没有 `default` 网络配置，则我们可以自己定义一个网络，通过 `default.xml ` 文件定义一个网络 :
> ```xml
> <!-- WARNING: THIS IS AN AUTO-GENERATED FILE. CHANGES TO IT ARE LIKELY TO BE OVERWRITTEN AND LOST. Changes to this xml configuration should be made using: virsh net-edit default or other application using the libvirt API. -->
> <network>
>   <name>default</name>
>   <uuid>e10f4d03-caa3-4fe6-a17b-c108733c62e6</uuid>
>   <forward mode='nat'/>
>   <bridge name='virbr0' stp='on' delay='0'/>
>   <mac address='52:54:00:59:c6:e6'/>
>   <ip address='192.168.122.1' netmask='255.255.255.0'>
>     <dhcp>
>       <range start='192.168.122.2' end='192.168.122.254'/>
>     </dhcp>
>   </ip>
> </network>
> ```
> 然后，通过 `sudo virsh net-define default.xml` 即可定义一个 `default` 网络配置

## 1.5 Images

最后，我们需要下载 Windows 镜像以及驱动镜像 :

- `Windows` - https://www.microsoft.com/zh-cn/software-download/windows11
- `virtio-win` - https://github.com/virtio-win/virtio-win-pkg-scripts/blob/master/README.md

# 02 Installation

## 2.1 kvm/qemu

我们通过 `virt-manager` 进行可视化安装，首先创建一个虚拟机 :

![[imgs/create_kvm_qemu.png]]

然后选择本地安装并选择需要使用的镜像 :

![[imgs/local_install.png|300]]![[imgs/choose_iso.png|300]]

然后，我们在分配好内存， CPU 以及磁盘后，勾选安装前配置的选项 :

![[imgs/set_to_config.png]]

接着，我们先确定是使用 UEFI 作为启动项 :

![[imgs/ensure_uefi.png]]

接着，我们选择将磁盘的总线改为 VirtIO ，这样能让虚拟机中的磁盘读取更快 :

![[imgs/disk_virtio.png]]

然后，将网络模型改为 `virtio` :

![[imgs/net_virtio.png]]

然后，将 Video QXL 选项改为 VirtIO :

![[imgs/video_virtio.png]]

接下来，我们需要将下载的驱动镜像挂载到虚拟机中，否则在安装 Windows 的时候就无法安装所需的驱动，导致无法安装。点击左下角的添加硬件，然后选择我们下载好的 `virtio-win` 镜像 :

![[imgs/virtio_iso_mount.png]]

然后，就是把 GPU 和音频设备挂载到虚拟机上 :

![[imgs/gpu_audio.png]]

最后，我们点击左上角开始安装，就能正常进入 Windows 的安装程序了。

## 2.2 Windows

在安装 Windows 的过程中，我们可能会遇到以下问题 :

- 无法找到安装磁盘
- 无法连接到网络

这是因为我们为磁盘，网络选择了 VirtIO 模式，但是却没有安装相应驱动的原因。在选择安装磁盘的界面，我们点击左下角的从文件安装驱动，并选择如下所示的文件夹查找驱动 :

![[imgs/virtio_place.png]]

找到驱动后安装即可。

在安装过程中，还建议跳过网络更新，通过创建本地账户的方式来安装，具体只需要在安装完的配置页面点击 `shift + f10` ，并在弹出的命令行窗口中执行 :

```powershell
oobe\BypassNRO.cmd 
```

系统会自动重启，并出现可以跳过网络链接的选项。

最后，系统安装完成后，我们还需要为系统安装相应的驱动，执行以下两个程序 :

![[imgs/full_virtio.png]]

将所有的驱动安装完即可。

# 03 Connection

通过 `virt-manager` 连接到虚拟机其实会有延迟和卡顿，在这里，我们选择使用远程桌面的服务来连接电脑 :

![[imgs/remote_control.png]]

在开启远程桌面的服务后，我们通过 `xfreerdp` 来连接。首先安装 :

```bash
sudo pacman -S freerdp
```

然后，我们查看虚拟机的 IP 地址 :

```bash
sudo virsh domifaddr win11-gpu
```

通过这个 IP 地址，我们就能直接连接到 Windows 上 :

```bash
xfreerdp3 /v:192.168.122.1 /u:blake /p:<you_password> /dynamic-resolution +clipboard /scale:140  
```