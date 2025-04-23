**Raidrive** 是一筐可以将云盘挂载到本地的工具，能够让我们轻松地管理云端的内容。 Raidrive 为 windows 提供了gui 界面，为 Linux 提供了 cli 命令。

# 01 Installation

在 Arch 下，Raidrive 为我们提供了 AUR 软件包 : 

```bash
yay -S raidrivecli
```

或者我们也可以访问官网查看下载教程。

# 02 Usage

在开始使用 `raidrivecli` 之前，我们应该启用 `raidrive` 的服务 : 

```bash
sudo systemctl enable --now raidrive.service
```

`raidrivecli` 为我们提供了如下的命令 : 

```text
Commands:
  add              add a virtual filesystem
  list             display all mountpoints
  show <label>     display properties
  edit <label>     edit properties
  remove <label>   remove mountpoints
  mount <label>    mount virtual filesystems
  unmount <label>  unmount virtual filesystems
  signin           sign in to take a license
  signout          sign out to return a license
  status           display using status
  set              display or set operation environment values
```

我们可以通过 `raidrivecli <command> help` 来查看具体的内容，例如，我们可以查看 `add` 命令的具体用法 : 

```text
Commands:
  alibaba                Alibaba Cloud
  aws                    AWS S3
  azure                  Azure
  azurechina             Azure for China
  backblaze              Backblaze B2
  box                    Box
  cloudflare             Cloudflare R2
  cloudian               Cloudian
  digitalocean           DigitalOcean Spaces
  directcloud            DirectCloud
  dropbox                Dropbox
  dropboxbusiness        Dropbox Business
  ftp <address>          FTP server
  gcp                    Google Cloud Platform
  googledrive            Google Drive
  googlephotos           Google Photos
  googleworkspace        Google Workspace
  ibm                    IBM Cloud
  idrive                 IDrive e2
  mailru                 Mail.ru Cloud
  mega                   MEGA
  minio                  MinIO
  ncp                    Naver Cloud Platform
  nhn                    NHN Cloud
  onedrive               OneDrive
  onedrivebusiness       OneDrive Business
  onedrivebusinesschina  OneDrive Business for China
  oracle                 Oracle Cloud
  pcloud                 pCloud
  s3                     AWS S3 compatible
  sftp <address>         SFTP server
  sharepoint             SharePoint
  sharepointchina        SharePoint for China
  tencent                Tencent Cloud
  wasabi                 Wasabi Cloud
  webdav <address>       WebDAV server
  yandex                 Yandex Disk
```

我们可以通过 `add` 添加上述提供的云盘服务，我们以 WebDAV 为例，通过 `raidrivecli add webdav --help` ，我们可以查看具体的添加方法 : 

```text
Description:
  WebDAV server

Usage:
  raidrivecli add webdav <address> [options]

Arguments:
  <address>  WebDAV URI (<http|https>://[username@]<host>[:port][/remote-path])

Options:
  -l, --label <label>                                      label for a virtual filesystem
  -m, --mount-path <path>                                  absolute local path as a mountpoint
  --read-only                                              make a mountpoint read-only
  --file-lock                                              prevent others from overwriting
  --public                                                 make a mountpoint accessible to others
  --mount-at-start                                         mount at daemon start [default: True]
  --prompt-credentials                                     mount using different credential
  --mount-now                                              mount if add success [default: True]
  --capacity <size>                                        force to set capacity (GB)
  --bandwidth-download <cps>                               throttled download traffic (MB/s)
  --bandwidth-upload <cps>                                 throttled upload traffic (MB/s)
  --keep-date-modified                                     try to keep modified date when copying
  --proxy <no|global|<scheme>://<username>@<host>:<port>>  proxy (scheme: http|socks4|socks4a|socks5)
  --proxy-pw <password>                                    proxy password
  -u, --username <username>                                username
  -p, --password <password>                                password
  --alt-address <url>                                      alternative url
  --tls <ssl30|tls10|tls11|tls12|tls13>                    tls version
  --http-timeout <seconds>                                 connection timeout seconds [default: 100]
  -?, -h, --help                                           Show help and usage information
```

可以看到，我们可以通过 : 

```bash
raidrivecli add webdav <url> [options]
```

来添加一个 WebDAV 服务。在他提供的 option 中，我们需要重点关注这几个 : 

- `-l, --label` - 为挂载的文件系统添加一个标签，建议设置成简洁明了的，可以指明网络服务的标签，后续删除或取消挂载的时候需要用到。
- `-m, --mount-path` - 为挂载的云盘指定一个挂载的路径
- `-u, --username` - 用于登录 webdav 服务的用户名
- `-p, --password` - 用于登录 webdav 服务的密码

因此，若想要将 infiniCloud 的盘挂载到本地 `~/infiniCloud` 目录下，我们可以 : 

```bash
raidrivecli add webdav https://chogo.teracloud.jp/dav/ -l infiniCloud -m ~/infiniCloud -u <username> -p <password>
```

我们还可以通过一下命令来查看所有挂载点及其信息 : 

```bash
raidrivecli list
```

然后，我们可以通过标签来删除或卸载一个云盘 : 

```bash
raidrivecli unmount infiniCloud # unmout the infiniCloud cloud drive
raidrivecli remove infiniCloud  # remove the mountpoint of infiniCloud cloud drive
```
