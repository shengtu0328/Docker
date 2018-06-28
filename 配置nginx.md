docker运行nginx
nginx是一个持久运行的容器，有别于helloworld在后台运行

从Docker中国官方镜像下载nginx镜像
docker pull registry.docker-cn.com/library/nginx

直接运行镜像 
docker run registry.docker-cn.com/library/nginx
(没有反应，因为在后台运行，ctrl+c结束运行)

显示所有运行的容器
docker ps

显示所有的容器
docker ps –a

后台运行容器，并显示出容器id
docker run -d registry.docker-cn.com/library/nginx

进入容器内部
