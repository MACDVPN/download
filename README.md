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
1.下载对应版本启动

2.启动会有报错找不到 geoip.db 与 geosite.db （记住找不到的文件路径）

3.前往 [geoip](https://github.com/SagerNet/sing-geoip/releases) 与 [geosite](https://github.com/SagerNet/sing-geosite/releases) 下载数据库

4.复制数据库到找不到文件的路径

5.再次启动

## 前端工程师已下班，还为上线可以管理版本，暂时无法使用控制台管理命令行版本节点，解决方法如下
1.访问 https://app.macdvpn.com 登录账号

2.点击键盘 F12 按照图片复制令牌
![Snipaste_2024-10-16_22-11-50](https://github.com/user-attachments/assets/2ebd9f6d-275b-4ea1-8625-fb3ff207321a)

3.访问 http://127.0.0.1:8888/account/set_token?account_id=XXX 设置令牌（XXX是您自己的令牌）

4.访问 http://127.0.0.1:8888/node/list 获取节点列表（如果令牌错误或无有效套餐会提示错误）

5.复制节点ID与接入点ID，如图（假设【01J4BHTS09XTV2EQNEE4PEC7PF是节点ID】【01J4BJ22WD36NNSG6X5C2RSA55是接入点ID】）
![Snipaste_2024-10-16_22-19-00](https://github.com/user-attachments/assets/a5e83298-bd5d-47a3-b9bd-af4b5fd5f039)

6.**访问 http://127.0.0.1:8888/node/test?node_id=01J4BHTS09XTV2EQNEE4PEC7PF&access_point_id=01J4BJ22WD36NNSG6X5C2RSA55 测试通信延迟（模拟访问谷歌通信）**

6.**访问 http://127.0.0.1:8888/node/test?node_id=01J4BHTS09XTV2EQNEE4PEC7PF&access_point_id=01J4BJ22WD36NNSG6X5C2RSA55 测试通信延迟（模拟访问谷歌通信）**

6.**访问 http://127.0.0.1:8888/node/test?node_id=01J4BHTS09XTV2EQNEE4PEC7PF&access_point_id=01J4BJ22WD36NNSG6X5C2RSA55 测试通信延迟（模拟访问谷歌通信）**

7.如果测试失败，请确保本机时间误差小于30秒，否则无法使用任何节点 [访问这个网站检查误差](https://time.is)

8.切换节点 http://127.0.0.1:8888/node/switch?node_id=01J4BHTS09XTV2EQNEE4PEC7PF&access_point_id=01J4BJ22WD36NNSG6X5C2RSA55 

9.查看当前节点ID与接入点ID http://127.0.0.1:8888/node/info

10.使用 HTTP / SOCKS 4/4a/5 / MIXED 连接代理

## 如果不会连接代理 HTTP / SOCKS 4/4a/5 / MIXED 代理请继续阅读
1.点击对应浏览器安装代理插件 [edge](https://microsoftedge.microsoft.com/addons/detail/fdbloeknjpnloaggplaobopplkdhnikc) [chrome](https://chromewebstore.google.com/detail/proxy-switchyomega/padekgcemlokbadohgkifijomclgjgif)

2.安装完成后请按照图片操作
![圖片](https://github.com/user-attachments/assets/b481e561-17ed-4ab9-82f7-6fd4ebe9d387)

![圖片](https://github.com/user-attachments/assets/3e284af4-d348-40c5-ba30-36147f16304a)

![圖片](https://github.com/user-attachments/assets/0b7f19d7-fbab-4902-9b6f-1d523bcf01ab)

![圖片](https://github.com/user-attachments/assets/e03bfe76-cde8-4f54-8f5b-b1c2d22f3185)

![圖片](https://github.com/user-attachments/assets/ef4f7447-1bb5-4bd9-8eb7-51b2908eb815)

### 全平台支持情况
命令行版本 - windows（已发布）

命令行版本 - mac（已发布）

命令行版本 - linux（已发布）

windows（最快下周发布）

macos（最快下周发布）

android（最快下月发布）

ios（待开发...）
