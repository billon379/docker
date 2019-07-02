##命令说明
>1. 参考文档：https://hub.docker.com/_/nginx/
>2. nginx容器配置文件目录/etc/nginx/conf.d/,使用-v将配置文件挂载到指定目录
```
docker run --detach \
    --name nginx \
    --restart always \
    --env TZ=Asia/Shanghai \
    --publish 80:80 --publish 443:443 \
    --volume ~/docker/nginx/conf.d/:/etc/nginx/conf.d/:ro \
    billon/nginx-alpine:1.15.5
```