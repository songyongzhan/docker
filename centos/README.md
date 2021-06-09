# 介绍

> 此dockerfile为纯净版本，内置了vim rzsz netstat 等基础功能

## 下载镜像地址

```bash

docker pull songsongyz/centos:1.0

```


## 通过Dokcerfile打包使用

```bash
 
 docker build -t songsongyz/centos:1.0 .

```
## 运行容器

```bash

docker run -itd --name myCentos songsongyz/centos:1.0

```



