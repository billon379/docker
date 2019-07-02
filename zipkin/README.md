##命令说明
>1. 参考文档：https://hub.docker.com/r/openzipkin/zipkin
```
docker run --detach \
    --name zipkin \
    --restart always \
    --env TZ=Asia/Shanghai \
    --env RABBIT_ADDRESSES=192.168.1.31:5672 \
    --env RABBIT_USER=billon \
    --env RABBIT_PASSWORD=billon \
    --env STORAGE_TYPE=elasticsearch \
    --env ES_HOSTS=192.168.1.31:9200 \
    --env ES_INDEX_SHARDS=1 \
    --env ES_INDEX_REPLICAS=1 \
    --publish 7999:9411 \
    billon/zipkin:2
```