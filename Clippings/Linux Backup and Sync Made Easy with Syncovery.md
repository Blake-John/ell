---
title: Linux Backup and Sync Made Easy with Syncovery
source: https://www.syncovery.com/linux-docs/
author: 
published: 2024-08-09
created: 2025-01-10
description: Get the most out of Syncovery on Linux and FreeBSD. Learn how to install Syncovery and manage your Linux Backup and Sync.
tags:
  - clippings
  - "#readed"
---
Welcome to the Syncovery Technical Documentation page for Linux and FreeBSD, your comprehensive guide to installing, configuring, and using the powerful backup and synchronization tool, Syncovery. Whether you’re a beginner looking to secure your files or an IT professional managing complex data workflows, this documentation provides step-by-step instructions, detailed explanations, and best practices to help you get the most out of Syncovery. From initial setup to advanced features, explore how Syncovery can seamlessly handle your backup and sync needs across multiple platforms with ease and reliability.

## Linux and FreeBSD Platforms that Syncovery Runs On

Syncovery runs on virtually all recent Linux and FreeBSD distributions as well as many NAS brands. It is available for various different CPU types, including Intel/AMD and ARM/AArch64 in both 32-bit and 64-bit.

Syncovery supports these **Linux** distributions and NAS systems:

- **Debian** and derived Linux types, including **Ubuntu**, Linux MINT, MX Linux, Kali Linux, **Raspberry Pi OS**, and many others
- **Red Hat** and distributions using the RPM package manager, including **Fedora, CentOS, openSUSE**, Rocky Linux and AlmaLinux
- Additional distributions where dpkg can be used, including **Arch Linux / Manjaro** and **Netgear ReadyNAS** devices
- Native installation packages are available for NAS models from **QNAP, Synology, ASUStor**, and Western Digital (WD)
- NAS models suported via our Unified Installer for Windows: **Seagate**, Thecus, and Zyxel.
- **FreeBSD** and derived systems, including **FreeNAS/TrueNAS** and XigmaNAS
- Simple tar.gz distribution packages are available for any other type of Linux

## Syncovery Installation Guides

Various methods are available to install Syncovery, your favorite Linux Backup and Sync software, on your system. Native installation packages exist in different formats, and generic tar.gz archives can also be used. If you are aware of the system and CPU type that you want to install Syncovery on, it is easy to pick the correct download. On the other hand, our Unified Syncovery Linux Installer is available to install Syncovery automatically and avoid having to pick a particular download package.

**After the installation**, you can reach Syncovery’s **web GUI via port 8999**. For example, enter the following line in your web browser (if your Linux system has a desktop GUI with browser):  
`localhost:8999`

If you are running your web browser on a different system, you need to enter the Linux system’s IP address, for example:  
`192.168.1.58:8999`

The initial **user name** is **default** and the password is **pass**.

![Screenshot showing Syncovery's login dialog](https://www.syncovery.com/wp-content/uploads/2024/08/login.jpg)

---

### The Unified Syncovery Linux Installer

The Unified Syncovery Linux Installer is a tool that runs on Windows and installs Syncovery on virtually all supported platforms using an SSH shell connection. You can use it if you have an SSH login that has admin or root privileges (or is allowed to use sudo). This useful installer tool is available from our [Syncovery for Linux Download Page](https://www.syncovery.com/download/linux/).

If you prefer to install Syncovery without using a Windows tool, you will find instructions for the different platforms in the following paragraphs:

### Installing Syncovery on a Synology NAS

You will find native installation packages for Synology on our [Syncovery Download Page for Synology NAS](https://www.syncovery.com/syncovery10synology/). These can be installed on Synology DSM 6 or 7 using the manual installation in Package Center. It is important to choose the correct download, depending on your CPU type and DSM version. In addition, if you have DSM 7 or later, you need to [grant Syncovery access](https://www.syncovery.com/syncovery-with-synology-dms-7/) to the folders that you want to work with.

### Installing Syncovery on a QNAP NAS

Our [QNAP Download Page](https://www.syncovery.com/syncovery10qnap/) contains packages for installation in the QNAP App Center, using the manual installation button. You will also find an older Syncovery version in the QNAP app catalog, but it is highly recommended to use the latest version directly from our web site. Please check which CPU your NAS has and download the correct package.

### Installing Syncovery on ASUStor, WD and others

Syncovery can be found in the [ASUStor App Central](https://www.asustor.com/app_central/app_detail?id=1555) and we also offer manual downloads on our [ASUStor Download Page](https://www.syncovery.com/syncovery10asustore/). There’s also a separate [download page for Western Digital (WD) NAS devices](https://www.syncovery.com/wd/). Additional NAS brands are supported by our [Unified Syncovery Linux Installer](https://www.syncovery.com/download/linux/).

### Installing Syncovery on Debian, Ubuntu, Linux MINT, Raspberry Pi, Netgear ReadyNAS and other Debian-based systems

Installation on these systems is done using the .deb packages. Please download the correct package from our [Linux Download Page](https://www.syncovery.com/syncovery10linux/) and install it, either using the installer that opens it on your Linux desktop, or using a Terminal or SSH shell window. Here’s an example for the installation command line:  
`sudo dpkg -i Syncovery-10.15.8-amd64.deb`

In some cases, dpkg may show an error, and if you are certain that you have the correct package, you can override any errors using this command line:  
`sudo dpkg -i --force-all Syncovery-10.15.8-amd64.deb`

### Installing Syncovery on Red Hat, Fedora, CentOS, openSUSE and other RPM-based systems

These systems use .rpm packages to install software, including Syncovery. Just download the correct RPM package from our [Linux Download Page](https://www.syncovery.com/syncovery10linux/) and install it with a command line such as:  
`sudo rpm -i Syncovery-10.15.8-amd64.rpm`

Alternatively, you can use yum:  
`sudo yum install Syncovery-10.15.8-amd64.rpm`

### Installation on FreeBSD, FreeNAS/TrueNAS and XigmaNAS

You will find installation instructions for FreeBSD based systems on our [FreeBSD Download Page](https://www.syncovery.com/freebsd/).

### Generic Linux Download Page

For an alternative overview of the installation types, including links to the various download pages, please see our [Generic Linux Download Page](https://www.syncovery.com/download/linux/).

---

## Using the Syncovery Web GUI for your Linux Backup and Sync

When you install a NAS, Debian or RPM package, the Web GUI should become available automatically.

If you choose the .tar.gz download, you can activate the web GUI by running these SyncoveryCL commands in a Terminal window:  
`./SyncoveryCL SET /WEBSERVER=localhost` *(to configure the web server)*  
`./SyncoveryCL start` *(to start SyncoveryCL – the start command line parameter is recognized since v8.25)*

Open the web GUI in a Browser window by entering: localhost:8999. Unless you are accessing the Web GUI from localhost, it will ask for username and password. The defaults are: user name = default, password = pass.

This is the complete command line to configure the web server:  
`SyncoveryCL SET /WEBSERVER=localhost /WEBUSER=username /WEBPASS=password /WEBPORT=port /WEBDOCSPATH=path_to_web_docs_folder`

To turn the web server OFF (requires a restart if SyncoveryCL is already running):  
`SyncoveryCL SET /WEBSERVER=OFF`

The Web Docs Folder is called WebDocs and it is included in the tar.gz archive that you download from this page.

## Additional Information

SyncoveryCL will create a .Syncovery folder for configuration, logs, and databases in the HOME folder. It depends on the HOME environment variable. You can also use SYNCOVERY\_HOME, which takes precedence. **HOME should not be /.**

## Syncovery Command Lines, not only for Linux Backup and Sync

Here are some example command lines to configure and run Syncovery. Additional command lines [can be found here](https://www.syncovery.com/command-line/). You only need to use command lines if the web GUI is not used or not ready yet.

Run a job without saving it to the configuration file:  
`SyncoveryCL RUN /LEFT="/home/tobias/Documents/" /RIGHT="/home/tobias/DocumentsCopy" /L2R`

Add this same job to the configuration file:  
`SyncoveryCL ADD /NAME="LocalTest" /LEFT="/home/tobias/Documents/" /RIGHT="/home/tobias/DocumentsCopy" /L2R`

Run an existing job:  
`SyncoveryCL /RUN="LocalTest"`

Configure a scheduled job (every 30 minutes):  
`SyncoveryCL ADD /NAME="LocalTest" /LEFT="/home/tobias/Documents/" /RIGHT="/home/tobias/DocumentsCopy" /L2R /Sched /Rep /Days=0 /Mins=30`

List Jobs in Config File:  
`SyncoveryCL /LIST`

Disable a job:  
`SyncoveryCL CHANGE "SFTPTest" /Disabled`

Enable a job:  
`SyncoveryCL CHANGE "SFTPTest" /Disabled=No`

Show job configuration:  
`SyncoveryCL SHOW "SFTPTest"`

---

The easiest way to get the command line with additional parameters is to create the job in the Windows or Mac version, and go to the Information tab sheet in the profile editor, where you will see the profile XML and command line.

---

Start the Scheduler (only necessary if you don’t use the Debian or RPM packages):  
`SyncoveryCL` *(runs in the foreground)*  
or  
`SyncoveryCL start` *(becomes a daemon – supported since v8.25)*  
or  
`SyncoveryCL &` *(runs in the background but not as a daemon)*

Stop the Scheduler:  
`SyncoveryCL /STOPTIMER`

See Scheduler Status:  
`SyncoveryCL /STATUS`

See Continuously Updated Scheduler Status:  
`SyncoveryCL /CONTSTATUS`

---

Upload to FTP:  
`SyncoveryCL ADD /NAME=FTPTest /LEFT="/home/tobias/Documents/" /RIGHT="ftp://username:password@yourdomain.com/FolderName" /L2R `

Upload to SFTP:  
`SyncoveryCL ADD /NAME=FTPTest /LEFT="/home/tobias/Documents/" /RIGHT="sftp://username:password@yourdomain.com/FolderName" /L2R `

Upload to SFTP with a certificate:  
`SyncoveryCL SET /CERT=/home/tobias/tobias_rsa    SyncoveryCL ADD /Name=WithKey /Left=/home/tobias /Right="sftp://tobiaskey@192.168.10.20/Tests" /L2R /RightFTPSettings="SFTP:Port=2222,AbsolutePath=N,Flags=UTF8+NoCertPass+UTC,"Cert=tobias_rsa""    SyncoveryCL /RUNX=WithKey /ACCEPTSERVER`

Upload to WebDAV (example: Strato HiDrive):  
`SyncoveryCL ADD /NAME=WebDAVTest /LEFT="/home/tobias/Documents/" /RIGHT="https://user:pass@webdav.hidrive.strato.com/users/yourusername/folder" /L2R /EXCL=.*`

Upload to Amazon S3:  
`SyncoveryCL ADD /LEFT="/home/tobias/Documents/" /RIGHT="S3://yourid:yoursecretkey{.:CRED:.}bucketname/Documents" /L2R /CacheDestination=Yes /EXCL=.* /NAME=S3Test`

Upload to Microsoft Azure:  
`SyncoveryCL ADD /NAME=AzureTest /LEFT="/home/tobias/Documents/" /RIGHT="AZ://yourid:yoursecretkey{.:CRED:.}container/Documents" /L2R`

Upload to Amazon Glacier:  
`SyncoveryCL ADD /NAME=GLTest /LEFT="/home/tobias/Documents/" /RIGHT="GL://yourid:yoursecretkey{.:CRED:.}vaultname/Documents" /L2R /EXCL=.*`

Upload to Rackspace:  
`SyncoveryCL ADD /LEFT="/home/tobias/Documents/" /RIGHT="ext://yourid:yourkey{.:CRED:.}containername/Documents" /RProt=Rackspace /L2R /EXCL=.* /NAME=RackTest`

Upload to SugarSync:  
`SyncoveryCL ADD /LEFT="/home/tobias/Documents/" /RIGHT="ext://your@email.com:yourpass{.:CRED:.}My SugarSync/Documents" /RProt=SugarSync /L2R /EXCL=.* /NAME=SugarTest`

Upload to Backblaze B2 Cloud Storage:  
`SyncoveryCL ADD /LEFT="/home/tobias/Documents/" /RIGHT="ext://account_id:application_key@BucketName/Documents" /RProt=B2 /L2R /NAME=B2Test`  
You can get your Account ID and Application Key from the “Buckets” page on Backblaze B2.

---

**Cloud Services with OAuth – a prompt will appear to open the OAuth URL in a browser.**

Upload to box.com:  
`SyncoveryCL ADD /LEFT="/home/tobias/Documents/" /RIGHT="ext://OptionalAcctID@Box/Documents" /RProt=Box /L2R /EXCL=.* /NAME=BoxTest`

Upload to Microsoft OneDrive:  
`SyncoveryCL ADD /LEFT="/home/tobias/Documents/" /RIGHT="ext://OptionalAcctID@OneDrvNew/Documents" /RProt=OneDrvNew /L2R /EXCL=.* /NAME=OneTest`

Upload to DropBox:  
`SyncoveryCL ADD /LEFT="/home/tobias/Documents/" /RIGHT="ext://DropBoxV2/Documents" /RProt=DropBoxV2 /L2R /EXCL=.* /NAME=DropBoxTest`

`SyncoveryCL /RUN=DropBoxTest`

---

**General Configuration**

Set up email noticiations using Gmail:  
`SyncoveryCL SET /GMAIL=youremail@gmail.com /SMTPPASS=xxx`

Specify mail recipients (if different from the Gmail address from previous command line):  
`SyncoveryCL SET /EmailRecipients=email1,email2,email3`

Apply global settings similar to the \[Main\] section of the INI file on Windows:  
`SyncoveryCL SET /SettingName=Value`

For example:  
`SyncoveryCL SET /S3PartSize=536870912`

Export a profile to XML:  
`SyncoveryCL /EXPORTONEXML="Profile Name"`

Import profile(s) from XML:  
`SyncoveryCL /IMPORT="/path/to/theprofiles.xml"`

See also [The Syncovery Command Line](https://www.syncovery.com/command-line/)

---

**Settings Dictionary for your Syncovery Linux Backup and Sync**  
You can download the complete dictionary of possible profile settings in pdf or xlsx format.  
[Syncovery Settings Dictionary PDF Document](https://www.syncovery.com/SyncoverySettingsDictionary.pdf "Syncovery Settings Dictionary PDF Document").  
[Syncovery Settings Dictionary Excel Document](https://www.syncovery.com/SyncoverySettingsDictionary.xlsx "Syncovery Settings Dictionary Excel Document").