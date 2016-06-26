
Docker Toolbox 是安裝 Docker 在 Windows 以及 Mac 上的建議方式. 透過一連串的 GUI 操作就可以安裝並設定完成 Docker Client, Docker Machine, Docker Compose, Docker Kitematic 以及 VirtualBox. 

Docker Toolbox 一整個就是懶人包的概念. 但是方便歸方便, 在 Mac 上面多少還是會希望能透過 Homebrew 方式來安裝, 同時也方便我們整理軟體安裝 Script 供未來重新安裝使用.

安裝方式有兩種

## 透過 Toolbox 安裝設定 Docker
---
這是最簡單的方式 XD

### 安裝 Toolbox 設定 Docker
```
$ brew cask install dockertoolbox
```

## 自行安裝設定 Docker
---

### 安裝 Docker 和 Docker-machine

```
$ brew install docker 
$ brew install docker-machine
```

### 建立及啟動 VM 

```
$ docker-machine create -d virtualbox default
```

### 確認 Docker-machine 的環境變數

```
$ docker-machine env default
export DOCKER_TLS_VERIFY="1"
export DOCKER_HOST="tcp://192.168.99.100:2376"
export DOCKER_CERT_PATH="/Users/hughyang/.docker/machine/machines/default"
export DOCKER_MACHINE_NAME="default"
# Run this command to configure your shell: 
# eval $(docker-machine env default)
```

### 設定 shell 的 docker 參數

```
$ echo 'eval "$(docker-machine env default)"' >> ~/.bash_profile
```