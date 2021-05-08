
#  `K8S 一键部署`
<br>
<br>

# 1.下载源码然后将里面的k8s配置文件拷贝到你所有的服务器

Gitee地址：https://gitee.com/bright-boy/xiyan-blog/tree/master/doc/k8s

Github地址：https://github.com/694475668/xiyan-blog/tree/master/doc/k8s


---
# 2.环境（根据你自己的服务器来选，一个master，一个node也可以，我这里三台服务器）
```
k8s1 192.168.80.130
k8s2  192.168.80.131
k8s3  192.168.80.132

```
---
# 3.下载的k8s配置文件详解
![输入图片说明](http://qiniu-picture.xiyanit.cn/FlNVlAST8etVecyDbRlk2T23C-7T "屏幕截图.png")

+ bin：相关一键启动脚本的目录

   * completeStartup.sh：完整版启动脚本

   * completeShutdown.sh：完整版关闭脚本

   * kernStartup.sh：核心版启动脚本【只包含必要的组件】

   * kernShutdown.sh：核心版关闭脚本

   * update.sh：用于更新镜像【同步最新代码时使用】

* config：存放配置文件

* data：存放数据文件

* k8s-install：一键部署K8S集群脚本

* k8s-upgrade：一键升级K8S集群脚本（可选）

* k8s-addNode：一键扩容K8S集群脚本（可选）

* yaml 各组件yaml文件

---
# 4.修改所有集群服务器的hostname
192.168.80.130

`hostnamectl set-hostname k8s1`

192.168.80.131

`hostnamectl set-hostname k8s2`

192.168.80.132

`hostnamectl set-hostname k8s3`

---
# 5.修改hosts（所有节点）
![输入图片说明](http://qiniu-picture.xiyanit.cn/FhvG0lqHfiQmkebrNagzDzTdiVYA "屏幕截图.png")

使用键盘工具可以同时在一个节点上修改所有节点的配置

`vi /etc/hosts`

```
192.168.80.130      k8s1
192.168.80.131      k8s2
192.168.80.132      k8s3
```
![输入图片说明](http://qiniu-picture.xiyanit.cn/FqFJ1DC15TD37YxBnRMPK693065X "屏幕截图.png")

---
# 6.将下载的k8s文件`上传到所有的集群服务器`
![输入图片说明](http://qiniu-picture.xiyanit.cn/FqbiIq4Wg2LDETA6-gqyAIeki5oN "屏幕截图.png")

授权完成后可以关闭键盘工具

```
chmod -R 777 k8s/
```

# 7.修改域名
![输入图片说明](http://qiniu-picture.xiyanit.cn/FvJ3LGsmYzBg1g1wBlJaAWQ04LxC "屏幕截图.png")

![输入图片说明](http://qiniu-picture.xiyanit.cn/FplNrAUDV-cxEES1AW_m5jsfQhLb "屏幕截图.png")

# 8.`master`执行脚本文件（务必关闭键盘工具）
## 8.1修改配置文件
![输入图片说明](http://qiniu-picture.xiyanit.cn/FkgBzkunpIjDSZCNhbZ3K8EhjsOS "屏幕截图.png")

## 8.2执行脚本
```
cd k8s/bin/

./kernStartup.sh

```
![输入图片说明](http://qiniu-picture.xiyanit.cn/Fv8OpX7wegtfAy7FRCWfHXEcOMAT "屏幕截图.png")

![输入图片说明](http://qiniu-picture.xiyanit.cn/FgStyqaWG63RnXnaBC0Cykun_IaI "屏幕截图.png")

## 8.3执行成功查看节点是否正常

```
kubectl get pod,svc -n xiyan
```
![输入图片说明](images/QQ截图20210323212856.png "屏幕截图.png")


# 9.支付配置
打开支付网页，刚刚你在nginx配置的域名   账户密码admin
![输入图片说明](http://qiniu-picture.xiyanit.cn/FilJRHtLmG979MXjBVFBKuGxTvZj "屏幕截图.png")
![输入图片说明](http://qiniu-picture.xiyanit.cn/FiFvUaUOEFlEB1CRB3NPREW2Im7E "屏幕截图.png")
![输入图片说明](http://qiniu-picture.xiyanit.cn/Fut_DlKxO0QHB8XBLyFfR4mtZgYR "屏幕截图.png")

---
# 10.修改nacos配置
打开http://ip8848/nacos  默认账户密码nacos

![输入图片说明](http://qiniu-picture.xiyanit.cn/FhKwRjdYvQ9fYJkVNEcMuKDnxUKC "屏幕截图.png")
![输入图片说明](http://qiniu-picture.xiyanit.cn/FiQxZXt3YWms0x4b6DEOOePEeQWe "屏幕截图.png")

---
# 11.重启xiyan-web-service服务

## 11.1 停止服务
```
kubectl delete -f xiyan-web-service.yaml
```
## 11.2 启动服务

```
kubectl apply -f xiyan-web-service.yaml
```

---
# 12.访问
用你刚刚配置的域名进行访问

![输入图片说明](http://qiniu-picture.xiyanit.cn/FmwJ2TRYKwKQEaO8P88--kTxa4Vk "屏幕截图.png")

---
# 13.如果没有运行成功，欢迎进群进行指导你
![输入图片说明](images/120440_39a64794_4856424_gaitubao_300x534.jpg "屏幕截图.png")