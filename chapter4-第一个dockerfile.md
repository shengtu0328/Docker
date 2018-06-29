dockerfile 的作用就是用来构建自己的镜像，规定每一步的操作
docker build 执行 dokerfile 里的每一件事，构建出一个镜像

1.构建一个自己的镜像（本例以jpress的war包作为 例子 ）
    访问 https://gitee.com/fuhai/jpress/tree/alpha/  点击wars 下载
    放到某个目录下 改个名
    mv jpress-web-newest.war jpress.war

2.下个tomcat镜像
    docker pull tomcat

3.新建一个Dockerfile 文件
   vi Dockfile
   from docker.io/tomcat

   MAINTAINER xiaoruiqing

   COPY jpress.war /usr/local/tomcat/webapps

  from是继承了docker.io/tomcat镜像
  MAINTAINER  作者
  COPY 把jpresswar包 放到 /usr/local/tomcat/webapps目录下

4.构建镜像
    在当前目录下构建镜像
    docker build .    



docker images 
发现没取名字


docker build -t jpress:latest .
给这个自定义镜像加个名字类型

发现有名字了


5.运行自己的镜像
docker run -d -p 8888:8080 jpress
检查一下


 




注意：tomcat 能访问 jpress不能访问，后来发现是jpress 的war包下错了   正确的war包大小是20m的
    
     

