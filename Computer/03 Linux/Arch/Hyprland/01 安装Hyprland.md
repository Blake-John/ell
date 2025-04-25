# 01 主体

Hyprland 在 Arch 上的安装及其简单，只需要在官方的软件包下载即可 

```bash
sudo pacman -S hyprland
```

> hyprland-git (AUR) - compiles from latest source
> hyprland - binary x86 tagged release

安装好 Hyprland 之后，我们就可以通过在终端中输入 `Hyprland` 来启动桌面环境。

当然，我们可以在 DM 中选择桌面环境来登录，这里推荐 `sddm` 。

```bash
sudo pacman -S sddm
sudo systemctl enable sddm
```

> [!tip]
> 如今 Hyprland 可以通过 UWSM (Universal Wayland Session Manager) 来管理会话，可以选择安装
> 
> ```bash
> yay -S uwsm
> ```
> 
> 此外，在 [AUR](https://aur.archlinux.org/packages?O=0&K=hyprland) 仓库中也有其他可供选择的安装项，用于适配 NVIDIA 或高分辨率屏幕

# 02 Utils

## 2.1 Must Have

### 2.1.1 Status Bar

对于一个系统来说，一个状态栏可以没有，但是其起到的作用十分巨大，最好要有。这里推荐使用 `waybar` 作为状态栏，其占用资源小，容易配置与抄作业，也易于使用，更有许多预设的组件以及文档供我们使用。

> [!seealso] 
> 相比于 `waybar` ， `eww` 有着更加轻量化的资源占用，但是其学习成本较高，用于定义的语法需要学习，不是常规的格式如 `json` 等

```bash
sudo pacman -S waybar
```

我们可以在 `hyprland.conf` 中在开始时启动 `waybar` : 

```conf
exec-once = waybar
```

### 2.1.2 Notification Daemon

系统需要一个通知守护进程，才能保证程序的信息能够发送到使用者手中，以免错过重要的信息。我们使用 `swaync` 作为我们的通知程序，主要有以下两个原因 : 

- 方便配置
- 有通知中心，更不容易错过重要消息

```bash
sudo pacman -S swaync
```

> [!seealso] 
> 如果觉得 `swaync` 不够轻量化，还可以选择使用 `dunst` , `mako` 等更加轻量化的通知程序

我们同样在 `hyprland.conf` 中启用 : 

```conf
exec-once = swaync
```

### 2.1.3 PipeWire and WirePlumber

`pipewire` 是一个多媒体框架，提供了音视频服务以及对音视频的捕获功能，可以实现屏幕的共享(录屏，截屏，投屏等功能)，而 `wireplumber` 则是在 `pipewire` 的基础上提供了模块化会话/策略管理的服务，包装了 `pipewire` 的 API : 

```bash
sudo pacman -S pipewire wireplumber
```

### 2.1.4 XDG-Desktop-Portal

`xdg-desktop-portal` 让应用程序与桌面环境/会话进行通信，实现文件的选择，屏幕的共享等功能 : 

```bash
sudo pacman -S xdg-desktop-portal xdg-desktop-portal-hyprland
```

XDP(xdg-desktop-portal) 和 XDPH(xdg-desktop-portal-hyprland) 会在启动的时候自动运行。如果运行没有问题，打开 `obs` 之后，选择录制屏幕，就会弹出一个窗口选择要录制的内容。为了确保 XDP 和 XDPH 正确运行，你可以设置在启动时运行以下脚本 `exec-once` : 

```bash
#!/usr/bin/env bash
sleep 1
killall -e xdg-desktop-portal-hyprland
killall xdg-desktop-portal
/usr/lib/xdg-desktop-portal-hyprland &
sleep 2
/usr/lib/xdg-desktop-portal &
```

### 2.1.5 Authentication Agent

一个授权服务用于在图形化界面输入密码授予权限。当应用需要使用高权限时，则 agent 会弹出一个窗口用于输入密码。我们使用 gnome 的 auth agent ，他更加轻量化，更加简便 : 

```bash
sudo pacman -S polkit-gnome
```

然后，我们在启动时运行该进程即可 : 

```conf
exec-once = /usr/lib/polkit-gnome/polkit-gnome-authentication-agent-1
```

### 2.1.6 Qt Wayland Support

我需要安装 qt 软件包插件使得 Qt 程序能在 wayland 上正确运行 : 

```bash
sudo pacman -S qt5-wayland qt6-wayland
```

## 2.2 Enhanced

### 2.2.1 Wallpaper

我们需要一个软件用于管理我们的壁纸。壁纸分为静态壁纸和动态壁纸，这里推荐使用 `swww` 来管理静态壁纸，使用 `mpvpaper` 来管理动态壁纸。

```bash
sudo pacman -S swww
yay -S mpvpaper
```

`swww` 是一个可以实时切换并加载静态壁纸的程序，且提供了较为精美(可自定义)的切换动画，占用系统资源小。我们只需要在启动时加载该程序并加载壁纸即可 : 

```conf
exec-once = swww-daemon
exec-once = swww img <path_to_wallpaper>
```

而 `mpvpaper` 则是一个用于将 `mp4` 等格式的视频作为壁纸，基于 `mpv` 播放器，占用系统的资源也很小，取决于要播放的视频的大小。

```bash
mpvpaper eDP-1 <path_to_mp4> -o loop > /dev/null 2>&1 &
```

### 2.2.2 App Launcher

我们使用 `rofi` 作为我们的程序启动器。 `rofi` 高度可自定义，且有详细的文档说明，我们可以通过 `rofi` 实现各种功能，不止启动应用。

```bash
sudo pacman -S rofi-wayland
```

> 如果安装了普通版本而不是 wayland 版本，则会出现一些问题

我们可以通过以下命令启动软件 : 

```bash
rofi -show drun -modi drun,window,filebrowser,run
```

### 2.2.3 Color Picker

我们将使用 `hyprpicker` 作为我们的颜色选择器，只需要启动并选择对应位置的颜色，即可获取其十六进制的颜色代码

```bash
sudo pacman -S hyprpicker
```

### 2.2.4 Clipboard Manager

我们使用 `rofi` 来选择我们的剪切板内容，使用 `cliphist` 作为我们的剪切板管理器，使用 `wl-clipboard` 来解码并使用剪切板 : 

```bash
sudo pacman -S cliphist wl-clipboard
```

我们首先需要启动 `cliphist` 来监听我们的复制操作 : 

```conf
exec-once = wl-paste --type text --watch cliphist store # Stores only text data

exec-once = wl-paste --type image --watch cliphist store # Stores only image data
```

然后，我们可以使用 `rofi` 展示我们的剪切板内容，可以使用和 app launcher 同样的样式 : 

```conf
bind = SUPER, V, exec, cliphist list | rofi -dmenu | cliphist decode | wl-copy
```

上面语句的意思是，把 `cliphist` 中的内容通过 `rofi` 列出，待 `rofi` 选择后，传回 `cliphist` 进行解码，最后通过 `wl-copy` 进行复制操作，使得下一次的粘贴为选中的内容。当然，我们也可以通过 `wl-paste` 直接进行粘贴。

```bash
wl-clipboard -o
```

### 2.2.5 File Manager

我们需要一个文件管理工具用于浏览并操作我们系统中的文件，分为 GUI 和 TUI 两种。GUI 工具有许多，比较推荐的是 : 

- **Dolphin** - KDE 文件管理工具
- **Nautilus** - Gnome 文件管理工具
- **Thunar** - Xfce 文件管理工具
- **PcmanFm-qt** - LXQt 文件管理工具
- **Krusader** - 默认双栏的文件管理工具

而 TUI 工具则推荐使用 `ranger` 。

> [!tip]
> GUI 工具可以根据安装的第二桌面的桌面环境来选择。
> 为什么要安装第二环境？
> ~~当然是防止 Hyprland 炸了，没有桌面环境来管理，维护系统啊~~

```bash
sudo pacman -S thunar dolphin nautilus krusader ranger
```

### 2.2.6 NetworkManager

我们在安装 Arch 的时候已经安装了 `networkmanager` ，但是缺少一个 GUI 界面来管理网络的连接，我们可以使用 `nm-applet` 来作为网络管理工具 : 

```bash
sudo pacman -S nm-applet
```

然后，我们在 `hyprland.conf` 中启动即可 : 

```conf
exec-once = nm-applet
```

### 2.2.7 Audio

接下来我们要安装一些相关的音频服务，使得我们能够控制我们的音量。在前面，我们已经安装了 `pipewire` 和 `wireplumber` 框架，接下来，我们就需要安装 GUI ， CLI 工具使得我们能够操控我们的音频，我们选择使用 `pavucontrol` 最为我们的 GUI 音频管理工具，使用 `pamixer` 作为我们的 CLI 管理工具 : 

```bash
sudo pacman -S pavucontrol pamixer
```

通过 `pavucontrol` ，我们可以很轻易地管理我们的音频设备，调整每一个应用的音量等，而 `pamixer` 则提供了快捷简便的 CLI 命令开管理整体的音量，控制扬声器的开关 (mute) 等。

除此之外，我们还需要安装 `pipewire` 和 `pulseaudio` 以及 `alsa` 沟通的包，以保证使用 `pulseaudio` 和 `alsa` 的应用能够正常运行 : 

```bash
sudo pacman -S pipewire-pulse pipewire-alsa
```

### 2.2.8 Bluetooth

我们通常情况下也会需要用到蓝牙，因此，我们需要安装蓝牙工具包 : 

```bash
sudo pacman -S bluez bluez-utils
```

`bluez` 提供了蓝牙服务，而 `bluez-utils` 则提供了 `bluetoothctl` 一系列用于操作蓝牙的命令。我们需要启动蓝牙相关服务才能使用 : 

```bash
sudo systemctl enable blutooth
```

> [!seealso] 
> 此外，我们也可以选择安装 `blueman` 作为我们的 GUI 蓝牙管理工具，同 `nm-applet` 一样

## 2.3 Hypr Ecosystem

### 2.3.1 hyprlock

我们通常需要一个锁屏工具，可以选择的有很多，最好用的是 `swaylock` , `hyprlock` ，前者提供了悬浮式锁屏，后者提供了全屏锁屏。这里推荐使用 `hyprlock` : 

```bash
sudo pacman -S hyprlock
```

官方给出了配置 `hyprlock` 的详细 [文档](https://wiki.hyprland.org/Hypr-Ecosystem/hyprlock/) ，配置过程较为简单，效果良好。具体可见 [05 组件](05%20组件.md) 中的相关部分。

### 2.3.2 hyprsunset

`hyprsunset` 提供了调整屏幕色温的功能，我们可以通过 `hyprsunset` 来调整我们屏幕的色温，让我们的屏幕变得暖起来 : 

```bash
sudo pacman -S hyprsunset
```

我们只需要在启动的时候执行即可 : 

```conf
exec-once = hyprsunset -t 6000
```

至此， Hyprland 已经成为一个完全体，其他桌面环境有的功能他都不缺乏，接下来，我们将对 Hyprland 进行 [优化配置](02%20配置Hyprland.md) 。

# 03 系统工具

## 3.1 输入法

我们选择使用 `fcitx5` 作为我们的输入法框架，并使用 `fcitx5-rime` 作为输入法引擎，使用 `rime-frost` 作为我们的输入法。

```bash
sudo pacman -S fcitx5 fcitx5-rime fcitx5-configtool
yay -S fcitx5-input-support
```

下载完 rime 引擎后，我们选择使用 `rime-frost` 作为我们的输入法。我们到 [GitHub - gaboolic/rime-frost: 白霜拼音](https://github.com/gaboolic/rime-frost) 上将仓库克隆到 `~/.local/share/fcitx5/rime` 下，即可完成配置。

```bash
git clone --depth 1 https://github.com/gaboolic/rime-frost ~/.local/share/fcitx5/rime
```

## 3.2 截屏录屏

> 在使用截屏录屏之前，确保 `pipewire` 能够正常运行

我们通过 `grimblast` 来完成屏幕的获取，通过 `swappy` 来完成截屏后图像简易的编辑，通过

## 3.3 