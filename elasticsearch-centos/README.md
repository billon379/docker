##命令说明
>1. 参考文档：https://hub.docker.com/_/elasticsearch/
>2. elasticsearch容器数据存储目录/usr/share/elasticsearch/data
>3. 重要：需要修改vm.max_map_count
```
docker run --detach \
    --name elasticsearch \
    --restart always \
    --env discovery.type=single-node \
    --publish 9200:9200 --publish 9300:9300 \
    --volume ~/docker/elasticsearch/data:/usr/share/elasticsearch/data \
    billon/elasticsearch-centos:6.4.3
```