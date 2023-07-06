# vscode的远程桌面

- 初次使用，请设置root用户的密码，在环境变量`ROOT_PASSWORD`中

## 启动命令：
```
docker run -tid --name vsc-remote --restart always \
-e ROOT_PASSWORD=yourpassword \
pch18/vsc-remote
```
