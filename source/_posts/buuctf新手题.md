---
title: buuctf新手题
top: false
comments: true
tags: CTF
top_img: https://w.wallhaven.cc/full/g7/wallhaven-g7wwoe.png    #点进文章的
cover: https://wx3.sinaimg.cn/mw690/0077G8Eply1gpkqio4azsj30bn06g0um.jpg    #界面外的
onlyTitle: true
---




**Crypto**
**1）篱笆墙的影子**
星星还是那颗星星哟 月亮还是那个月亮 山也还是那座山哟 梁也还是那道梁 碾子是碾子 缸是缸哟 爹是爹来娘是娘 麻油灯呵还吱吱响 点的还是那么丁点亮 哦哦 注意：得到的 flag 请包上 flag{} 提交

```xml
felhaagv{ewtehtehfilnakgw}
```

  栅栏密码

```xml
flag{wethinkwehavetheflag}
```


解密 ：13
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210415204710624.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

加密 ：2

![在这里插入图片描述](https://img-blog.csdnimg.cn/2021041520473320.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)
**2）Rabbit**

```xml
U2FsdGVkX1/+ydnDPowGbjjJXhZxm2MP2AgI
```

rabbit编码

```xml
flag{Cute_Rabbit}
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210415204834830.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

**3）Quoted-printable**

```xml
=E9=82=A3=E4=BD=A0=E4=B9=9F=E5=BE=88=E6=A3=92=E5=93=A6
```



```xml
flag{那你也很棒哦}
```


![在这里插入图片描述](https://img-blog.csdnimg.cn/20210415204957390.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

**4）变异凯撒**
```xml
加密密文：afZ_r9VYfScOeO_UL^RWUc
```


这里我们发现a, f, Z, _的ASCii码是 97， 102， 90， 95

而再看这里flag{}的ASCii码是--------102，108，97，103；

这时你会发现                                   5   ， 6   ，7 ，  8

```xml
flag{Caesar_variation}
```
**5）password**

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210415205612410.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210415205638581.png)

就是弱口令了
就是姓和名的首字母和出生年月日

```xml
flag{zs19900315}
```

**6）摩丝（摩斯）**


![在这里插入图片描述](https://img-blog.csdnimg.cn/20210415210306499.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

```xml
.. .-.. --- ...- . -.-- --- ..-
```

交错的莫尔斯电码

```xml
flag{iloveyou}
```


```xml
flag{ILOVEYOU}
```

小写没过大写过了
因为摩斯电码在设计的时候就没有区分大小写，而且从码表中可以看到，都是大写，所以在网站上解密出来的自己转成大写
**7）看我回旋踢（凯撒）**

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210415205934502.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

```xml
synt{5pq1004q-86n5-46q8-o720-oro5on0417r1}
```

拼不齐的flag  和{} 凯撒

```xml
flag{5cd1004d-86a5-46d8-b720-beb5ba0417e1}
```


**8）一眼就解密**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210415210055661.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

```xml
ZmxhZ3tUSEVfRkxBR19PRl9USElTX1NUUklOR30=
```

有一个“=” 64base
![](https://img-blog.csdnimg.cn/20210415210024156.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

flag{THE_FLAG_OF_THIS_STRING}

**9）url编码**

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210415210130744.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

```xml
%66%6c%61%67%7b%61%6e%64%20%31%3d%31%7d
```

直接url编码

```xml
flag{and 1=1}
```

**10）md5**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210415210214759.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)


```xml
e00cf25ad42683b3df678c61f42c6bda
```


md5在线解码

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210415210222198.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

```xml
admin1
```


```xml
flag{admin1}
```


