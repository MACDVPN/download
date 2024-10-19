## 默认代理
```
HTTP: 127.0.0.1:8080
```

```
SOCKS 4/4a/5 127.0.0.1:1080
```

```
MIXED 127.0.0.1:18080
```

### 命令行版本使用教程
1.下载对应版本启动（运行错误版本会无法启动）

2.启动会有报错找不到 geoip.db 与 geosite.db （记住找不到的文件路径）

3.前往 [geoip](https://github.com/SagerNet/sing-geoip/releases) 与 [geosite](https://github.com/SagerNet/sing-geosite/releases) 下载数据库

4.复制数据库到找不到文件的路径

5.再次启动

6.访问 https://app.macdvpn.com 登录账号

7.确认订阅有效

8.访问 https://app.macdvpn.com/dash_board/proxy/node 强制打开节点管理

## 错误日志
注意！不是所有错误都是有致命性！
注意！以下错误信息也可能会出现在api错误信息，处理方法保持一致

如出现以下错误日志：只需等待片刻即可，软件正在获取服务端点 automatically retrieving...
```
{"level":"error","error":"endpoint does not exist, automatically retrieving...","time":"......","message":"call"}
```

如出现以下错误日志：只是软件在后台与服务端点通信，无任何影响，不必关注
```
{"level":"error","error":"...... dialing to the given TCP address timed out","time":"......","message":"do"}
```
```
{"level":"error","error":"timeout","time":"......","message":"do"}
```
```
{"level":"error","error":"read tcp4 ......: wsarecv: An existing connection was forcibly closed by the remote host.","time":"......","message":"do"}
```

如出现以下错误日志：原因是没有设置节点请查看上方设置节点教程
```
{"level":"error","error":"unsupported network type","time":"......","message":"handler"}
```

### 全平台支持情况
命令行版本 - windows（已发布）

命令行版本 - mac（待编译）

命令行版本 - linux（待编译）

windows（最快下周发布）

macos（最快下周发布）

android（最快下月发布）

ios（待开发...）
