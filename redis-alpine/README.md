##命令说明
>1. 参考文档：https://hub.docker.com/_/redis/
>2. redis持久化数据在容器中的存储路径为/data,使用-v挂载宿主机目录存储redis数据
>3. 如果使用自定义的redis.conf,配置文件中的daemonize yes必须注释掉,否则容器无法启动
```
docker run --detach \
    --name redis \
    --restart always \
    --env TZ=Asia/Shanghai \
    --publish 6379:6379 \
    --volume ~/docker/redis/data:/data \
    --volume ~/docker/redis/redis.conf:/etc/redis.conf:ro \
    billon/redis-alpine:4.0.11
```