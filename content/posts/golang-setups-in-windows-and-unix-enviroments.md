---
weight: 6
title: Golang setups in Windows and Unix enviroments
date: 2023-08-22T03:39:45.363Z
lastmod: 2023-08-22T03:39:45.375Z
draft: false
author: codephilosopher
authorLink: https:/github.com/codephilosopher/codeman-blog
lightgallery: true
toc:
  auto: true
---
S﻿etup **Golang** is not that hard. To install *golang* your can go to [golang downloads](https://go.dev/dl/) .

**W﻿indows**

If you are going to install on windows you can download windows binaries of 32/64 architects 

![windows binaries](/images/uploads/screenshot-from-2023-08-22-12-05-41.png)

if you are planning to download the compressed files, you  have to set path variables in system environment.

or you can install  the installer with *msi*  version, which will install and do all the  necessary settings for you.

y﻿ou can also work  with Linux environment using Windows Subsystem for Linux ([WSL](https://en.wikipedia.org/wiki/Windows_Subsystem_for_Linux)) .

W﻿indows has provided good article for installing WSL in your machine [wsl installtion](https://learn.microsoft.com/en-us/windows/wsl/install)

**L﻿inux**

Go [binary distributions](https://golang.org/dl/) are available for these supported operating systems and architectures. Please ensure your system meets these requirements before proceeding. If your OS or architecture is not on the list, you may be able to [install from source](https://golang.org/doc/install/source) or [use gccgo instead](https://golang.org/doc/install/gccgo). 

![](/images/uploads/screenshot-from-2023-08-22-12-26-20.png)

Download the archive and extract it into /usr/local, creating a Go tree in /usr/local/go. For example:

```shell
tar -C /usr/local -xzf go.x.tar.gz

```

### Setup Go Environment

Add this to your **~/.bashrc** file

GOROOT is the location where Go package is installed on your system.

```shell
export GOROOT=/usr/local/go

```

\
GOPATH is the location of your work directory. For example my project directory is ~/go, you can create what ever folder structure you want.

```shell
export GOPATH=$HOME/go

```

Sytem wide PATH setting

```shell
export PATH=$GOPATH/bin:$GOROOT/bin:$PATH
```



If you want to install to any specific Linux distribution, lets say Fedora.

you can install with the command 

```shell
sudo dnf install golang
```

this will install latest stable version in your system. 

To check the go version installed in your system

```shell
go version

```

t﻿his will show the go version in your terminal

![](/images/uploads/screenshot-from-2023-08-22-12-42-45.png)

Get all go evironment variable settings.

```shell
go env
```

![](/images/uploads/screenshot-from-2023-08-22-12-45-52.png)