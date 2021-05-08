#  `docker-compose 一键部署`
<br>
<br>

# 1.下载源码然后将里面的docker-compose配置文件拷贝到你的服务器

Gitee地址：https://gitee.com/bright-boy/xiyan-blog


Github地址：https://github.com/694475668/xiyan-blog


![输入图片说明](http://qiniu-picture.xiyanit.cn/FvejY2aFvtzk_zZRl9ynFQEqchys "屏幕截图.png")


![输入图片说明](http://qiniu-picture.xiyanit.cn/FqNQt3IfOwl7COBujI1hqdlJBrZG "屏幕截图.png")


---

# 2.目录介绍
* bin：相关一键启动脚本的目录

   * completeStartup.sh：完整版启动脚本

   * completeShutdown.sh：完整版关闭脚本

   * kernStartup.sh：核心版启动脚本【只包含必要的组件】

   * kernShutdown.sh：核心版关闭脚本

   * update.sh：用于更新镜像【同步最新代码时使用】

* config：存放配置文件

* data：存放数据文件

* log：存放日志文件

* yaml：存放docker compose的yaml文件
---
# 3.授权
```
chmod -R 777 /usr/local/docker-compose

chmod 644 -R /usr/local/docker-compose/config/elfk/

```
---
# 4.修改nginx配置改为你配置的域名
`vim /usr/local/docker-compose/config/nginx/xiyan.conf`

![输入图片说明](http://qiniu-picture.xiyanit.cn/Fi03KpCL7OvztgZHxQDJlvn9R01c "屏幕截图.png")

---
# 5.如果服务器是4g以下的请开启虚拟内存，4g以上请忽略
Linux开启虚拟内存:  http://xiyanit.cn/article?id=10

---
# 6.安装Docker
Centos7下Docker安装:  http://xiyanit.cn/article?id=30

---
# 7.安装docker compose (三种方式任选其一)
docker-compose的安装:  http://xiyanit.cn/article?id=29

---

# 8.部署
```
cd /usr/local/docker-compose/bin/


sh kernStartup.sh
```
![输入图片说明](http://qiniu-picture.xiyanit.cn/Fi1VvyEg7s8G4O8A6hW6Vey7uC9k "屏幕截图.png")

---
# 9.查看是否都启动成功
`docker ps -a;`
![输入图片说明](http://qiniu-picture.xiyanit.cn/FsL1vJyHukuqPO_Lvi7kYx9vBWGc "屏幕截图.png")

---
# 10.支付配置
打开支付网页，刚刚你在nginx配置的域名   账户密码admin
![输入图片说明](http://qiniu-picture.xiyanit.cn/FilJRHtLmG979MXjBVFBKuGxTvZj "屏幕截图.png")
![输入图片说明](http://qiniu-picture.xiyanit.cn/FiFvUaUOEFlEB1CRB3NPREW2Im7E "屏幕截图.png")
![输入图片说明](http://qiniu-picture.xiyanit.cn/Fut_DlKxO0QHB8XBLyFfR4mtZgYR "屏幕截图.png")

---
# 11.修改nacos配置
打开http://ip8848/nacos  默认账户密码nacos

![输入图片说明](http://qiniu-picture.xiyanit.cn/FhKwRjdYvQ9fYJkVNEcMuKDnxUKC "屏幕截图.png")
![输入图片说明](http://qiniu-picture.xiyanit.cn/FiQxZXt3YWms0x4b6DEOOePEeQWe "屏幕截图.png")

---
# 12.重启xiyan-web-service服务
打开http://ip:9000

![输入图片说明](http://qiniu-picture.xiyanit.cn/Fr-Ara75uRvGrrA7PuL56PdqAS6r "屏幕截图.png")

选择本地docker连接

![输入图片说明](http://qiniu-picture.xiyanit.cn/Fu3PuaC_Tnnh841dMQl-DUPwoqJM "屏幕截图.png")

---
# 13.访问
用你刚刚配置的域名进行访问

![输入图片说明](http://qiniu-picture.xiyanit.cn/FmwJ2TRYKwKQEaO8P88--kTxa4Vk "屏幕截图.png")

---
# 14.如果没有运行成功，欢迎进群进行指导你
![输入图片说明](images/120440_39a64794_4856424_gaitubao_300x534.jpg "屏幕截图.png")