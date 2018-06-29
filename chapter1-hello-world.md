
Centos7 安装 docker
yum install docker
 
查看docker 版本
docker version
 
启动docker 服务
service docker start
 
拉取镜像
docker pull name :TAG
docker pull hello-world
name是镜像名称(必填)
TAG是版本(不必填，不填代表拉取的是最新版本)
默认是去官网下
 
查看本地所有镜像（IMAGE_ID唯一标识镜像）
docker images repository :TAG 
repository 是镜像名
 
运行容器
docker run image :TAG
image是镜像(必填)
docker run hello-world
 
docker帮助命令
docker run –help
 
显示所有运行的容器
docker ps
 
显示所有的容器
docker ps –a

删除镜像  
docker rmi docker.io/tomcat

停止容器
docker stop 7
