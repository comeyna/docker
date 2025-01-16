## v2rayA

一个易用而强大的，跨平台的 V2Ray 客户端。你可通过本节对用户文档的内容进行快速预览。

## 镜像

```
docker pull mzz2017/v2raya
```

## docker compose

```
services:
  v2raya:
    image: mzz2017/v2raya
    container_name: v2raya
    restart: always
    privileged: true
    network_mode: host
    environment:
      - V2RAYA_LOG_FILE=/tmp/v2raya.log
    volumes:
      - /lib/modules:/lib/modules:ro
      - /etc/resolv.conf:/etc/resolv.conf
      - /etc/v2raya:/etc/v2raya
```

## 相关地址

github：https://github.com/v2rayA/v2rayA

docker：https://hub.docker.com/r/mzz2017/v2raya

文档：https://v2raya.org/