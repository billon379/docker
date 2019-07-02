##命令说明
>1. 参考文档：https://hub.docker.com/_/mysql/
>2. 使用-e指定参数,MYSQL_ROOT_HOST(root用户登录ip),MYSQL_ROOT_PASSWORD(root用户密码)
>3. mysql内的配置文件目录为/etc/mysql/conf.d
>4. 容器内的数据库文件写入地址为/var/lib/mysql
>5. 修改时区--env TZ=Asia/Shanghai
>6. 发现一个bug,直接使用MYSQL_ROOT_PASSWORD_FILE环境变量会提示文件不存在,使用MYSQL_ROOT_PASSWORD运行以后就正常了
```
docker run --detach \
    --name mysql \
    --restart always \
    --env TZ=Asia/Shanghai \
    --env MYSQL_ROOT_HOST=% \
    --env MYSQL_ROOT_PASSWORD=root \
    --publish 3306:3306 \
    --volume ~/docker/mysql/data:/var/lib/mysql \
    billon/mysql-debian:5.7
```