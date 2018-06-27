# Docker1
Docker入门

Centos7 安装 docker
yum install docker


启动docker 服务
service docker start


run的时候没有这个容器会去官方下这个镜像
 

docker ps –a   目前所有的容器：

docker ps      显示所有运行的容器：

docker images  查看本地所有镜像（IMAGE_ID唯一标识镜像）
docker build  -t jpress:latest ./test/       -t 是命名  jpress 是名字  latest 版本  ./test/
docker run -d -p 8888:8080 jpress      -d标识后台运行 –p表示端口映射name  
