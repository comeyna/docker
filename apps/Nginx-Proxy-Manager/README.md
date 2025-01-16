## Nginx Proxy Manager

在您的网络上公开 Web 服务。使用 Let's Encrypt 免费提供 SSL。设计时充分考虑了安全性。非常适合家庭网络。

## 镜像

```
docker pull jc21/nginx-proxy-manager:latest
```

## docker compose

```
services:
  app:
    image: jc21/nginx-proxy-manager:latest
    container_name: npm
    volumes:
      - ./data:/data
      - ./letsencrypt:/etc/letsencrypt
    ports:
      - 80:80
      - 81:81
      - 443:443
    restart: unless-stopped
```

## 登录账号

```
账号 admin@example.com
密码 changeme
```

## 相关地址

官方：https://nginxproxymanager.com/