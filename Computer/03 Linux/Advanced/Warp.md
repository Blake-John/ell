# 00 Introduction

**warp** is a modern terminal for linux and macos.

# 01 Quick Start

## 1.1 Install Warp

### 1.1.1 For Arch

The easiest way to install Warp is to download the [x64 .pkg.tar.zst package](https://app.warp.dev/download?package=pacman) or [ARM64 pacman package](https://app.warp.dev/download?package=pacman_arm64). After downloading, you can install the package with:

```bash
sudo pacman -U ./<file>.pkg.tar.zst
```

The first time you update Warp through the app, it will guide you through **setting up the Warp pacman repository and signing key**.

Alternatively, you can manually configure the Warp pacman repository and install Warp by running the following commands:

```bash
sudo sh -c "echo -e '\n[warpdotdev]\nServer = https://releases.warp.dev/linux/pacman/\$repo/\$arch' >> /etc/pacman.conf"
sudo pacman-key -r "linux-maintainers@warp.dev"
sudo pacman-key --lsign-key "linux-maintainers@warp.dev"
sudo pacman -Sy warp-terminal
```

### 1.1.2 For Ubuntu

The easiest way to install Warp is to download [x64 .deb package](https://app.warp.dev/download?package=deb) or [ARM64 deb package](https://app.warp.dev/download?package=deb_arm64). After downloading, you can install the package with:

```bash
sudo apt install ./<file>.deb
```

Installing the .deb package will **automatically set up the Warp apt repository and signing key** needed to automatically update Warp and verify the integrity of the downloaded packages.

Alternatively, you can manually configure the Warp apt repository and install Warp by running the following commands:

```bash
sudo apt-get install wget gpg
wget -qO- https://releases.warp.dev/linux/keys/warp.asc | gpg --dearmor > warpdotdev.gpg
sudo install -D -o root -g root -m 644 warpdotdev.gpg /etc/apt/keyrings/warpdotdev.gpg
sudo sh -c 'echo "deb [arch=amd64 signed-by=/etc/apt/keyrings/warpdotdev.gpg] https://releases.warp.dev/linux/deb stable main" > /etc/apt/sources.list.d/warpdotdev.list'
rm warpdotdev.gpg
sudo apt update && sudo apt install warp-terminal
```