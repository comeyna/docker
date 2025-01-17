## 3x-UI

3x-UI 是一个用来管理和配置 Xray（一个网络代理工具）配置的 Web 用户界面（UI）。

## 镜像

```
docker pull ghcr.io/mhsanaei/3x-ui:latest
```

## docker compose

```
services:
  3x-ui:
    image: ghcr.io/mhsanaei/3x-ui:latest
    container_name: 3x-ui
    hostname: rahn
    volumes:
      - ./db/:/etc/x-ui/
      - ./cert/:/root/cert/
    environment:
      XRAY_VMESS_AEAD_FORCED: "false"
      X_UI_ENABLE_FAIL2BAN: "true"
    tty: true
    network_mode: host
    restart: unless-stopped
```

## 登录帐号

```
端口 2053
帐号 admin
密码 admin
```

## 相关地址

官方：https://github.com/MHSanaei/3x-ui