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

### 命令行版本使用教程（软路由版本）（请确保你有一定的电脑技术）
1.下载对应版本启动（运行错误版本会无法启动）

2.启动会有报错找不到 geoip.db 与 geosite.db （记住找不到的文件路径）

3.前往 [geoip](https://github.com/SagerNet/sing-geoip/releases) 与 [geosite](https://github.com/SagerNet/sing-geosite/releases) 下载数据库

4.复制数据库到找不到文件的路径

5.再次启动

## 前端工程师已下班，还为上线可以管理版本，暂时无法使用控制台管理命令行版本节点，解决方法如下
1.访问 https://app.macdvpn.com 登录账号

2.点击键盘 F12 按照图片复制令牌
![1](https://github.com/user-attachments/assets/604d4a6a-6ec6-4a05-96fa-cd218f514fab)

3.访问 http://127.0.0.1:8888/account/set_token?account_id=XXX 设置令牌（XXX是您自己的令牌）

4.访问 http://127.0.0.1:8888/node/list 获取节点列表（如果令牌错误或无有效套餐会提示错误）

5.复制节点ID与接入点ID，如图（假设【01J4BHTS09XTV2EQNEE4PEC7PF是节点ID】【01J4BJ22WD36NNSG6X5C2RSA55是接入点ID】）
![1](https://github.com/user-attachments/assets/7b15d595-4be1-4513-b663-f2538f71e460)

**6.访问 http://127.0.0.1:8888/node/test?node_id=01J4BHTS09XTV2EQNEE4PEC7PF&access_point_id=01J4BJ22WD36NNSG6X5C2RSA55 测试通信（模拟访问谷歌）**

**6.访问 http://127.0.0.1:8888/node/test?node_id=01J4BHTS09XTV2EQNEE4PEC7PF&access_point_id=01J4BJ22WD36NNSG6X5C2RSA55 测试通信（模拟访问谷歌）**

**6.访问 http://127.0.0.1:8888/node/test?node_id=01J4BHTS09XTV2EQNEE4PEC7PF&access_point_id=01J4BJ22WD36NNSG6X5C2RSA55 测试通信（模拟访问谷歌）**

7.如果测试失败，请确保本机时间误差小于30秒，否则无法使用任何节点 [访问这个网站检查误差](https://time.is)

8.切换节点 http://127.0.0.1:8888/node/switch?node_id=01J4BHTS09XTV2EQNEE4PEC7PF&access_point_id=01J4BJ22WD36NNSG6X5C2RSA55 

9.查看当前节点ID与接入点ID http://127.0.0.1:8888/node/info

10.使用 HTTP / SOCKS 4/4a/5 / MIXED 连接代理

## 错误日志
注意！不是所有错误都是有致命性！
注意！以下错误信息也可能会出现在api错误信息，处理方法保持一致

如出现以下错误日志：只需等待片刻即可，软件正在获取服务端点 automatically retrieving...
```
{"level":"error","error":"api endpoint does not exist, automatically retrieving...","time":"......","message":"call"}
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
