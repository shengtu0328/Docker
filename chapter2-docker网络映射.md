在浏览器中访问 nginx

1).docke容器的三种网络类型（bridge,host,none）
   
   每一个networknamespace提供了独立的网络

    bridge（docker默认）：独立拥有一个networknamespace
    host ：代表和主机用的同一个网卡,共用一个networknamespace (在docker里面使用网络和主机是一样的)
    none：不会和外界进行通讯
    选择了 bridge，如果需要容器的端口在主机上访问到，就需要和主机上的端口的映射。

  
eth0 是主机的网卡

关闭容器
docker stop 7
7是这个容器id的第一位，因为目前只有一个容器，所以可以这样关。

docker run -d -p 8080:80 registry.docker-cn.com/library/nginx 
p代表开放一个容器的端口到主机上（Publish a container's port(s) to the host (default [])）
8080是主机的端口
80是容器的端口
registry.docker-cn.com/library/nginx 是容器的名字




查看8080端口的网络连接情况
netstat -na|grep 8080


在主机浏览器上打开localhost:8080




容器所有的端口都会和主机建立映射
docker run -d -P registry.docker-cn.com/library/nginx 
主机32768 容器80



































