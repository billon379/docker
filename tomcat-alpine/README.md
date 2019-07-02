##命令说明
>1. 参考文档：https://hub.docker.com/_/tomcat/
>2. CATALINA_HOME:/usr/local/tomcat,可以使用-v将web工程的war包直接挂载到/usr/local/tomcat/webapps路径
```
docker run --detach \
    --name tomcat8.5 \
    --restart always \
    --env TZ=Asia/Shanghai \
    --publish 8888:8080 \
    --volume ~/docker/tomcat/webapps:/usr/local/tomcat/webapps \
    billon/tomcat-alpine:8.5
```