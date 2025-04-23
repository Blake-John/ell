---
category: Misc
tags:
  - "#bug"
  - "#problem"
  - "#arch"
desc: 用于记录使用 Arch Linux 中遇到的问题
author: Blake John
list:
  - 已解决
  - 未解决
---
# 01 Pacman

## 1.1 GPGME Error #solved

```Text
╭─  ~ 6ms 
╰─> sudo pacman -Syu                                                                                                                                            blake@Zero at 09:59:44 
[sudo] blake 的密码：
错误：GPGME 错误：无数据
错误：GPGME 错误：无数据
错误：GPGME 错误：无数据
:: 正在同步软件包数据库...
 core                                                                             115.6 KiB   445 KiB/s 00:00 [##################################################################] 100%
 extra                                                                              7.6 MiB  3.19 MiB/s 00:02 [##################################################################] 100%
 multilib                                                                         132.2 KiB  1574 KiB/s 00:00 [##################################################################] 100%
 archlinuxcn 已经是最新版本
 warpdotdev 已经是最新版本
错误：GPGME 错误：无数据
错误：GPGME 错误：无数据
错误：GPGME 错误：无数据
错误：未能同步所有数据库（未预期的错误）
```

### Desc

在使用 pacman 更新软件的时候，无法正常完成

### Solution

将 `/var/lib/pacman/sync/*.sig` 中的 `.sig` 文件删除即可 : 

```bash
- sudo rm -rf /var/lib/pacman/sync/.sig
```

### Reason

pacman在更新数据库文件时也会尝试下载 `$repo.db.sig`，这里的 `$repo` 可以是 `core` , `extra` , `community` , `archlinuxcn` 等仓库。

但是无论是官方源还是 archlinuxcn 源，**大多数源的数据库文件**都不会被签名，也就**不会存在 `.db.sig 文件`**。

pacman 尝试下载时这些数据库文件的签名文件时，镜像站就会返回 **404 的 http 状态码** 表示文件不存在，因此会出现 `GPGME 无数据` 的错误。

而出现这种错误的情况大多是发生在 **校园网** 、酒店免费 WIFI 这种 **需要登陆以后才能上网的网络环境**。

因为 pacman 尝试下载 `.db.sig` 文件时被登陆网页劫持了（这点你们应该深有感受，如果你在这种网络环境下没有登陆，你无论访问什么网页都会被重定向到登录界面，http 的状态码此时是200，不是404）。从没见过 `.db.sig` 的 pacman 此时两眼放光，由于没有挨骂，他就迅速地把登录界面当成是`.db.sig`下载下来了。

下载下来以后，pacman 激动地摆弄起 `.db.sig`，甚至发现里面没有自己期待已久的 GPG签名数据并开始报错时仍然不愿意撒手，因此此时无论再怎么同步源码、再怎么 `Syyu` 也不会有效果，必须人工干预。

## 1.2 unknown trust #solved 

```text
signature from "frederik Schwan <frederik.schwan@linux.com>" is unknown trust
```

### Desc

在使用 pacman 下载软件的时候，通常为安装系统的时候，无法通过密钥验证

### Solution

导入正确的密钥 : 

```bash
sudo pacman -S archlinux-keyring
```

### Reason

没有安装正确的密钥导致软件包的验证无法通过。

# 02 SDDM

## 2.1 Socket Session

### Desc

当我们使用 `sddm-greeter --theme /usr/share/sddm/theme/sugar-candy` 时，会出现 : 

```text
╭─  ~ 2s87ms
╰─> sddm-greeter --theme /usr/share/sddm/themes/sugar-candy
[17:37:44.887] (II) GREETER: High-DPI autoscaling Enabled
[17:37:44.912] (II) GREETER: Reading from "/usr/local/share/wayland-sessions/hyprland-uwsm.desktop"
[17:37:44.912] (II) GREETER: Reading from "/usr/share/wayland-sessions/hyprland-uwsm.desktop"
[17:37:44.912] (II) GREETER: Reading from "/usr/local/share/wayland-sessions/hyprland.desktop"
[17:37:44.912] (II) GREETER: Reading from "/usr/share/wayland-sessions/hyprland.desktop"
[17:37:44.912] (II) GREETER: Reading from "/usr/local/share/wayland-sessions/xfce-wayland.desktop"
[17:37:44.912] (II) GREETER: Reading from "/usr/share/wayland-sessions/xfce-wayland.desktop"
[17:37:44.913] (II) GREETER: Reading from "/usr/local/share/xsessions/xfce.desktop"
[17:37:44.913] (II) GREETER: Reading from "/usr/share/xsessions/xfce.desktop"
[17:37:44.913] (II) GREETER: Loading theme configuration from "/usr/share/sddm/themes/sugar-candy/theme.conf"
[17:37:44.919] (EE) GREETER: Socket error:  "QLocalSocket::connectToServer: Invalid name"
[17:37:44.919] (EE) GREETER: Cannot connect to the daemon - is it running?
```

### Solution

#tobesolved

## 2.2 Could not load the sugar-candy theme

### Desc

无法正常加载 sugar-candy 的主题，并有红色字报错。

### Solution

安装相应的qt包如 `qt5-quickcontrols2` 等，建议直接安装整个 `qt` 软件包组

# 03 link

## 3.1 无法使用

有时创建的软链接为红色的，并且不可用，这是因为软链接需要使用 **绝对路径** 来创建，否则在 **其他路径下** 将无法识别。

![[imgs/red_link_error.png]]