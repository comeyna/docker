## Alist

一个支持多种存储的文件列表程序，使用 Gin 和 Solidjs。

## 镜像

```
docker pull xhofe/alist:latest
```

## docker compose

```
services:
    alist:
        image: xhofe/alist:latest
        container_name: alist
        volumes:
            - ./data:/opt/alist/data
            - /root:/root
            - /etc:/etc
        ports:
            - 5244:5244
        restart: unless-stopped
```

## 密码设置

```
# 随机生成一个密码
docker exec -it alist ./alist admin random
# 手动设置一个密码,`NEW_PASSWORD`是指你需要设置的密码
docker exec -it alist ./alist admin set 1
```

## 相关地址

官方：https://alist.nn.ci/zh/

文档：https://alist.nn.ci/zh/guide/install/docker.html