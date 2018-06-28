Docker运行nginx
nginx是一个持久运行的容器，有别于helloworld在后台运行

从Docker中国官方镜像下载nginx镜像
docker pull registry.docker-cn.com/library/nginx

直接运行镜像 
docker run registry.docker-cn.com/library/nginx
(没有反应，因为在后台运行，ctrl+c结束运行)

后台运行容器，并显示出容器id
docker run -d registry.docker-cn.com/library/nginx

进入容器内部
在容器的内部执行一个命令
docker exec –help
docker exec –it 7 bash
i是保证输入有效
t分配一个伪终端
7是容器的id的第一个字（因为只有一个容器，所以可以输这个容器id的第一个字母）
 
进入容器之后，其实进入了一个虚拟机（linux目录结构）
 
 

查看这个放nginx的container有哪些进程
ps –ef 全格式显示当前所有的进程
 
发现没有ps命令
执行
apt-get update 
apt-get install procps
后成功显示
 


退出容器 
exit
 
