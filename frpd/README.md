# frp内网穿透快速部署 - 服务端

```
docker run -tid --name frps --net=host --restart always \
-e ADMIN_USER=username \
-e ADMIN_PWD=password \
-e TOKEN=ttttttken \
pch18/frpd
```