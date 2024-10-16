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
![1](https://github.com/user-attachments/assets/604d4a6a-6ec6-4a05-96fa-cd218f514fab)

3.访问 http://127.0.0.1:8888/account/set_token?account_id=XXX 设置令牌（XXX是您自己的令牌）

4.访问 http://127.0.0.1:8888/node/list 获取节点列表（如果令牌错误或无有效套餐会提示错误）

5.复制节点ID与接入点ID，如图（假设【01J4BHTS09XTV2EQNEE4PEC7PF是节点ID】【01J4BJ22WD36NNSG6X5C2RSA55是接入点ID】）
![1](https://github.com/user-attachments/assets/7b15d595-4be1-4513-b663-f2538f71e460)

6.如果测试失败，请确保本机时间误差小于30秒，否则无法使用任何节点 [访问这个网站检查误差](https://time.is)

7.切换节点 http://127.0.0.1:8888/node/switch?node_id=01J4BHTS09XTV2EQNEE4PEC7PF&access_point_id=01J4BJ22WD36NNSG6X5C2RSA55 

8.查看当前节点ID与接入点ID http://127.0.0.1:8888/node/info

9.使用 HTTP / SOCKS 4/4a/5 / MIXED 连接代理

## geosite导致的兼容性问题（下个版本更新解决）
请删除 config.json 文件中如下规则，不删除可能导致http代理无法正常使用
![Snipaste_2024-10-17_06-43-17](https://github.com/user-attachments/assets/04160b2d-e5dc-4245-8f09-40681759efce)


## 如果不会连接代理 HTTP / SOCKS 4/4a/5 / MIXED 代理请继续阅读
1.点击对应浏览器安装代理插件 [edge](https://microsoftedge.microsoft.com/addons/detail/fdbloeknjpnloaggplaobopplkdhnikc) [chrome](https://chromewebstore.google.com/detail/proxy-switchyomega/padekgcemlokbadohgkifijomclgjgif)

2.安装完成后请按照图片操作
![1](https://github.com/user-attachments/assets/cd7f22c1-6f5c-402f-9c4d-8709e244fc14)
![1](https://github.com/user-attachments/assets/0ce3f83f-c239-41d8-b444-228c6d05ba96)
![1](https://github.com/user-attachments/assets/39428412-f124-4954-a4cc-ac7a5b562729)
![1](https://github.com/user-attachments/assets/f43b4315-40d6-4927-9a2b-ecc2bad7c0bc)
![1](https://github.com/user-attachments/assets/b4613abb-7b8c-4976-b4b5-bdfbeeea9395)

### 全平台支持情况
命令行版本 - windows（已发布）

命令行版本 - mac（已发布）

命令行版本 - linux（已发布）

windows（最快下周发布）

macos（最快下周发布）

android（最快下月发布）

ios（待开发...）
