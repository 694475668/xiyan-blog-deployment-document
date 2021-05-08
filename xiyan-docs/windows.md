# `Windows 部署`
<br>
<br>
<br>


# `1. 下载项目源码`

Gitee地址：https://gitee.com/bright-boy/xiyan-blog

Github地址：https://github.com/694475668/xiyan-blog

---

# `2. 安装博客之前请将JDK安装，mysql数据库安装，IntelliJ IDEA安装`

### 工具下载地址：http://xiyanit.cn/tool

如安装有问题，进群咨询

##  `安装完将下载源码里面的sql导入到数据库中`
![输入图片说明](images/sd.png "屏幕截图.png")
![输入图片说明](images/my.png "屏幕截图.png")

---
# `3. nacos部署`

#### nacos下载地址，直接运行就可以用，我都已经配置好了的： 

链接：https://pan.baidu.com/s/1PJ6TLQdN_uOdAEjo56BgAw 

提取码：cyu5 

![输入图片说明](images/QQ截图20210323161212.png "屏幕截图.png")

## 3.1访问地址ip:8848/nacos 默认用户名密码都是nacos
![输入图片说明](images/QQ截图20210323161410.png "屏幕截图.png")
![输入图片说明](images/QQ截图20210323161511.png "屏幕截图.png")
![输入图片说明](images/QQ截图20210323161735.png "屏幕截图.png")
![输入图片说明](images/QQ截图20210323170419.png "屏幕截图.png")

---
# `4. redis部署`

链接：https://pan.baidu.com/s/1wfxpoGHe3Hbn62EZWI7LJg

提取码：wsi1 

#### redis下载地址，直接运行就可以用，我都已经配置好了的： 
![输入图片说明](images/QQ截图20210323162554.png "屏幕截图.png")
![输入图片说明](images/QQ截图20210323162916.png "屏幕截图.png")

---
# `5. sentinel部署（可选）`
链接：https://pan.baidu.com/s/1BJZBZJhpuzIhon6-M09j_w

提取码：xy6w 

```
java -jar sentinel-dashboard-1.8.0.jar --server.port=8888

```
![输入图片说明](images/QQ截图20210323163320.png "屏幕截图.png")

## ip:8888 进行访问，默认用户名密码都是sentinel

![输入图片说明](images/QQ截图20210323163447.png "屏幕截图.png")

---

# `6. elasticsearch部署`

链接：https://pan.baidu.com/s/1-vvgBp7wxVu7FS7DIynOHw

提取码：xvf4 

## 6.1 双击bin目录下的【elasticsearch.bat】即可启动es，默认启动后占用9200端口
![输入图片说明](images/20190821165256447.png "屏幕截图.png")

## 6.2可通过【http://127.0.0.1:9200/ 】访问 
![输入图片说明](images/20190821165738667.png "屏幕截图.png")

---

# `7. seata部署`

链接：https://pan.baidu.com/s/1jM7EEaAJSX1G05roK6wMbw 

提取码：b2v6 

![输入图片说明](images/QQ截图20210323175736.png "屏幕截图.png")
![输入图片说明](images/QQ截图20210323175907.png "屏幕截图.png")

---

# `8. zipkin部署（可选）`

链接：https://pan.baidu.com/s/1ULFMCGcNDCubG-ypvoXHsA 

提取码：vi3x 

```
java -jar -Xms64m -Xmx128m zipkin-server-2.12.9-exec.jar
```
![输入图片说明](images/QQ截图20210323205135.png "屏幕截图.png")

---

# `9. kafka部署`

链接：https://pan.baidu.com/s/1Hj3e3QDAvM5UnA8HSGi8Ww

提取码：zbdt 

## 9.1运行zookeeper
```
zookeeper-server-start.bat zookeeper.properties
```
## 9.2在开一个窗口运行kafka

```
kafka-server-start.bat server.properties
```
![输入图片说明](images/QQ截图20210323205729.png "屏幕截图.png")

![输入图片说明](images/QQ截图20210323205352.png "屏幕截图.png")
![输入图片说明](images/QQ截图20210323205433.png "屏幕截图.png")

---

# `10. xxl-job部署`

![输入图片说明](images/QQ截图20210323210101.png "屏幕截图.png")
![输入图片说明](images/QQ截图20210323210302.png "屏幕截图.png")

---

# `11. 后端部署`
![输入图片说明](images/QQ截图20210323210429.png "屏幕截图.png")
![输入图片说明](images/QQ截图20210323210612.png "屏幕截图.png")

---

# `12. 前端部署`

```
npm install
```


```
npm run dev
```
## 12.1 部署成功数据都已获取

![输入图片说明](images/QQ截图20210323210847.png "屏幕截图.png")

---
# 13.如果没有运行成功，欢迎进群进行指导你
![输入图片说明](images/120440_39a64794_4856424_gaitubao_300x534.jpg "屏幕截图.png")

