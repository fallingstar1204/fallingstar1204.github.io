---
layout: post
title: "Install docker on Mac"
date: 2016-07-02 16:27:53 +0800
comments: true
categories: Docker Homebrew
---

在 Mac 上安裝 Docker 的方式有兩種

- [透過 Toolbox 安裝設定 Docker](#toolbox)
- [自行安裝設定 Docker](#manaul)


### <span id="toolbox">透過 Toolbox 安裝設定 Docker</span>
這是最簡單的方式! Docker Toolbox 是安裝 Docker 在 Windows 以及 Mac 上的建議方式. 透過一連串的 GUI 操作就可以安裝並設定完成 Docker Client, Docker Machine, Docker Compose, Docker Kitematic 以及 VirtualBox. 說明白一點就是懶人包 XD

##### 透過安裝 Toolbox 設定 Docker
```
$ brew cask install dockertoolbox
```

### <span id="manaul">自行安裝設定 Docker</span>

##### 安裝 Docker 和 Docker-machine

```
$ brew install docker 
$ brew install docker-machine
```

##### 建立及啟動 VM 

```
$ docker-machine create -d virtualbox default
```

##### 確認 Docker-machine 的環境變數

```
$ docker-machine env default
export DOCKER_TLS_VERIFY="1"
export DOCKER_HOST="tcp://192.168.99.100:2376"
export DOCKER_CERT_PATH="/Users/hughyang/.docker/machine/machines/default"
export DOCKER_MACHINE_NAME="default"
# Run this command to configure your shell: 
# eval $(docker-machine env default)
```

##### 設定 shell 的 docker 參數

```
$ echo 'eval "$(docker-machine env default)"' >> ~/.bash_profile
```