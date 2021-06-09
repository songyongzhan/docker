# docker-nginx 安装使用

两种使用方法

## 一、下载Dockerfile安装使用

### 1. 下载 Dockerfile 打包成镜像安装

> docker build -f Dockerfile -t songyongzhan/nginx:1.0 .

### 2. 运行容器

docker 文件记录


## 二、下载docker镜像使用

```bash
docker pull 
```



## 三、运行docker

```bash
docker run -itd --name my-nginx-2 -p 8080:80 -v /root/docker/nginx_git/logs:/usr/local/nginx/logs -v /root/docker/nginx_git/xm_data:/data -v /root/docker/nginx_git/conf:/usr/local/nginx/conf 22b6def4f8fa
```
