##命令说明
>1. 参考文档：https://hub.docker.com/_/jenkins/
>2. jenkins数据和插件存储目录为/var/jenkins_home,使用-v将配置文件挂载到指定目录
```
docker run --detach \
    --name jenkins \
    --restart always \
    --env TZ=Asia/Shanghai \
    --publish 8080:8080 --publish 50000:50000 \
    --volume ~/docker/jenkins/:/var/jenkins_home \
    billon/jenkins-alpine:2.60.3
```