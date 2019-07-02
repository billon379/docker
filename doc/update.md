##更新日志(2019-06-13)
>1. 修改nginx,redis,rabbit镜像版本

##更新日志(2019-03-22)
>1. 新增zipkin配置

##更新日志(2019-01-08)
>1. 新增redis自定义配置说明

##更新日志(2018-11-15)
>1. 新增elasticsearch-centos配置说明
>2. 新增kibana-centos配置说明

##更新日志(2018-07-20)
>1. 修改mysql-debian/my.cnf,修改mysql sql_mode

##更新日志(2018-07-09)
>1. 修改mysql-debian/my.cnf,让数据库支持emoji字符

##更新日志(2018-06-20)
>1. 新增Dockerfile(rabbitmq-alpine:3.7.6)

##更新日志(2018-04-02)
>1. 修改docker-compose,gitlab启动时环境参数设置有问题

##更新日志(2018-03-29)
>1. 修改Dockerfile(jdk-alpine),删除fontconfig,新增ttf-dejavu
>2. 修改Dockerfile(jenkins-alpine),删除fontconfig
>3. 修改Dockerfile(tomcat-alpine),删除fontconfig,新增ttf-dejavu
>4. 修改Dockerfile(tomcat-alpine),解决tomcat启动慢问题

##更新日志(2018-03-29)
>1. 修改Dockerfile(jdk-alpine),新增tzdata,fontconfig
>2. 修改Dockerfile(jenkins-alpine),新增tzdata,fontconfig
>3. 修改Dockerfile(tomcat-alpine),新增tzdata,fontconfig
>4. 修改Dockerfile(redis-alpine),新增tzdata

##更新日志(2018-03-27)
>1. 修改Dockerfile(tomcat-alpine),新增修改tomcat配置的脚本
>2. 删除Dockerfile(gitlab-ubuntu),时区使用ENV定义
>3. 删除Dockerfile(nexus-centos),时区使用ENV定义
>4. 修改Dockerfile(jdk-alpine),时区变量名使用TZ
>5. 修改Dockerfile(jenkins-alpine),时区变量名使用TZ
>6. 修改Dockerfile(redis-alpine),时区变量名使用TZ
>7. 修改Dockerfile(nginx-alpine),时区使用ENV定义

##更新日志(2018-03-26)
>1. 发现一个bug,直接使用MYSQL_ROOT_PASSWORD_FILE环境变量会提示文件不存在,使用MYSQL_ROOT_PASSWORD运行以后就正常了

##更新日志(2018-03-19)
>1. 新增Dockerfile(gitlab-ubuntu:ce)
>2. 修改Dockerfile(mysql-debian),删除修改my.cnf权限的命令
>3. 修改Dockerfile(nexus-centos),时区使用ENV定义
>4. 修改README.md,命令部分换行

##更新日志(2018-03-17)
>1. mysql数据库字符集修改，编译镜像时载入配置文件
>2. mysql密码从文件读取
>3. mysql时区设置
>4. md代码部分使用代码块儿标记
>5. docker-compose.yml修改为v3版本
>6. 修改docker容器时区为Asia/Shanghai
>7. redis镜像CMD命令直接加载配置文件

##更新日志(2018-03-04)
>1. 新增Dockerfile(nexus:3)

##更新日志(2018-02-22)
>1. 新增Dockerfile(jdk-alpine:8)
>2. 新增Dockerfile(nginx-alpine:1.13.8)
>3. 新增Dockerfile(redis-alpine:4.0.8)
>4. 新增Dockerfile(mysql-debian:5.7)
>5. 新增Dockerfile(tomcat-alpine:8.5)
>6. 新增Dockerfile(jenkins-alpine:2.60.3)
>7. 新增Dockerfile(gitlab-ubuntu)