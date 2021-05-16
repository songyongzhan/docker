FROM songsongyz/pure-centos:1.0
MAINTAINER 574482856@qq.com

RUN yum -y install make
RUN yum -y install gcc pcre-devel zlib-devel openssl openssl-devel
# http://nginx.org/en/download.html
# 安装不同的版本 直接更改版本号即可
ENV NGINX_VERSION nginx-1.18.0

ENV SRC_DIR /usr/local/src

RUN cd $SRC_DIR && wget http://nginx.org/download/$NGINX_VERSION.tar.gz

RUN tar -xf $SRC_DIR/$NGINX_VERSION.tar.gz -C $SRC_DIR/

ENV NGINX_DIR /usr/local/nginx

RUN mkdir -p $NGINX_DIR

# 编译并安装
RUN cd $SRC_DIR/$NGINX_VERSION && ./configure --prefix=/usr/local/nginx --with-http_ssl_module &&  make && make install

# 真正使用的时候需要将 logs data conf 挂载到外面
# 容器内的路径
# logs   /usr/local/nginx/logs
# data   /data
# conf  /usr/local/nginx/conf

# 开放的端口
EXPOSE 80
EXPOSE 443

# 开机启动
CMD ["/usr/local/nginx/sbin/nginx", "-g", "daemon off;", "-c", "/usr/local/nginx/conf/nginx.conf"]
