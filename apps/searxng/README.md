## SearXNG

SearXNG 是一款免费的互联网元搜索引擎，它汇总了来自各种搜索服务和数据库的结果。它不会跟踪或分析用户。

## 镜像

```
docker pull searxng/searxng:latest
```

## docker compose

```
services:
  searxng:
    image: searxng/searxng:latest
    container_name: searxng
    ports:
      - 8061:8080
    volumes:
      - ./data:/etc/searxng:rw
    cap_drop:
      - ALL
    cap_add:
      - CHOWN
      - SETGID
      - SETUID
    logging:
      driver: 'json-file'
      options:
        max-size: '1m'
        max-file: '1'
    restart: unless-stopped
```


## 相关地址

Github：https://github.com/searxng/searxng