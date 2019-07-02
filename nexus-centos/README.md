##命令说明
>1. 参考文档：https://hub.docker.com/r/sonatype/nexus3/
>2. nexus数据存储目录/nexus-data
>3. 需要修改nexus挂载目录的权限``` chown -R 200 ```,否则启动报错
```
docker run --detach \
    --name nexus \
    --restart always \
    --env TZ=Asia/Shanghai \
    --publish 8090:8081 \
    --volume ~/docker/nexus/nexus-data:/nexus-data \
    billon/nexus-centos:3
```