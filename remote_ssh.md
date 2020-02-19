# 远程连接服务器

## 方案一

* 端口号
  * 211服务器 60401
  * 212服务器 60402
  * 213服务器 60403
  * 214服务器 60404
  * 215服务器 60405
  * 216服务器 60406
```
ssh yourname@182.92.197.175 -p 某端口号

# 如宋宏伟在214机器
ssh songhongwei@182.92.197.175 -p 60404
```
* 注意事项
  * 只有terminal文本界面
  * 带宽有限，尽量避免从服务器向本地机拷贝大量数据
  
* Matlab用户？
  * 可命令行运行脚本（.m文件）

* 带宽限制问题解决方案？
  * 暂时无。返校后将尝试向网络中心，为服务器申请固定IP。

## 方案二

* 下载 [easyconnect](https://sslvpn.zjweu.edu.cn/com/installClient.html) 连接到学校的 vpn
  * URL: https://ivpn.hit.edu.cn
 
* 查看实验室路由器的 ip 地址：https://github.com/splab604/resources/blob/master/RouterIp.md
  * 实验室路由器 ip 地址不是固定的，需要在 `RouterIp.md` 中查看最新的 ip 地址
 
* 登录远程桌面
  
  ```bash
  # x = 1~5, 端口 3389x 对应 211 到 215
  <路由器 ip>:3389x
  
  # 例如登录 211 服务器远程桌面
  172.17.233.19:33891
  ```
  
* ssh
  
  ```bash
  # 2221x: x = 1~5
  ssh -p 2221x <username>@<路由器 ip>
  
  # 例如连接 211 服务器
  ssh -p 22211 lijianchen@172.17.233.19
  ```
