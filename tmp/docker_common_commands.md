## 註冊及登入 Docker Hub
[Docker Hub][DockerHubWebsite] 上存放許多 docker image 供大家使用, 建議註冊一個帳號來用.

```
$ docker login
```

## Image 相關 
---
|指令|說明|
|:---|:---|
|$ docker pull [OPTIONS] NAME[:TAG \| @DIGEST] | Pull an image or a repository from a registry|
|$ docker images [OPTIONS] [REPOSITORY[:TAG]] | List images|
|$ docker rmi [OPTIONS] IMAGE [IMAGE...] | Remove one or more images |


## Container 相關
---

|指令|說明|
|:---|:---|
|$ docker run [OPTIONS] IMAGE [COMMAND] [ARG...] | Run a command in a new container |
|$ docker rm [OPTIONS] CONTAINER [CONTAINER...] | Remove one or more containers |


## Repository 相關
---


[DockerHubWebsite]:https://hub.docker.com/