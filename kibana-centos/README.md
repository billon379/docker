##命令说明
>1. 参考文档：https://hub.docker.com/_/kibana/
```
docker run --detach \
    --name kibana \
    --restart always \
    --env ELASTICSEARCH_URL=http://${host:port} \
    --publish 5601:5601 \
    billon/kibana-centos:6.4.3
```