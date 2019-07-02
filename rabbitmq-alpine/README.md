##命令说明
>1. 参考文档：https://hub.docker.com/r/library/rabbitmq/
```
docker run --detach \
    --name rabbitmq \
    --restart always \
    --publish 5671:5671 --publish 5672:5672 \
    --publish 4369:4369 --publish 25672:25672 \
    --publish 15671:15671 --publish 15672:15672 \
    billon/rabbitmq-alpine:3.7.8
```