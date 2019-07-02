##命令说明
>1. 参考文档：https://docs.gitlab.com/omnibus/docker/
>2. gitlab容器数据存储目录/etc/gitlab
>3. gitlab容器日志目录/var/log/gitlab
>4. gitlab容器配置文件目录/var/opt/gitlab
>5. gitlab并发超过30会出现403,修改``` gitlab_rails['rack_attack_git_basic_auth'] ```
```
docker run --detach \
    --name gitlab \
    --restart always \
    --env TZ=Asia/Shanghai \
    --env GITLAB_OMNIBUS_CONFIG="external_url 'http://gitlab.example.com/'; gitlab_rails['gitlab_shell_ssh_port'] = 2222" \
    --hostname gitlab.example.com \
    --publish 8081:80 --publish 2222:22 \
    --volume ~/docker/gitlab/config:/etc/gitlab \
    --volume ~/docker/gitlab/logs:/var/log/gitlab \
    --volume ~/docker/gitlab/data:/var/opt/gitlab \
    billon/gitlab-ubuntu:ce
```