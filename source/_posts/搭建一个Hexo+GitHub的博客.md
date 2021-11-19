---
title: 搭建一个hexo+GitHub博客
tags: 小黑屋挖宝
toc: true
---
新新补充：目录设置。
新补充：电脑更换系统或更换电脑博客的重新部署，由于电脑原因我重现下了系统。
<!--more-->
## 一：搭建前的环境准备
### （1）Node.js 的安装和准备
在浏览器上**搜索node**
![node的官网](https://img-blog.csdnimg.cn/20210130135932142.png)
点进去**下载**
![下载任意一个](https://img-blog.csdnimg.cn/20210130140015158.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)
**按步骤安装**
![!\[安装\](https://img-blog.csdnimg.cn/20210130140104847.png](https://img-blog.csdnimg.cn/20210130140547217.png)


**[详细安装过程](https://blog.csdn.net/antma/article/details/86104068)**
### （2）git的安装和准备 
浏览器搜索**git**
![搜索](https://img-blog.csdnimg.cn/20210130140646320.png)
点进去后，点击如图：
![点击](https://img-blog.csdnimg.cn/20210130140712144.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)
![点击](https://img-blog.csdnimg.cn/20210130140758563.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)
安装
![安装](https://img-blog.csdnimg.cn/20210130140841914.png)
[Git详细安装](https://blog.csdn.net/yaojxing/article/details/72902973)

### （3）gitHub账户的配置
先注册GitHub账号：[地址](https://github.com/)
登陆之后，点击页面右上角的加号，选择New repository：
![这样](https://img-blog.csdnimg.cn/20210130141601182.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

进入代码库创建页面：
在Repository name下填写 你的昵称.github.io，如图所示：
![e](https://img-blog.csdnimg.cn/20210130141700177.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

**注意：比如我的github名称是yuanwangmumu，这里你就填 yuanwangmumu.github.io。就是填成你的昵称.github.io这种格式**

## 二：环境配置及其相关问题解决
桌面右键点开 git bash here
进入命令框

```xml
node -v
```

```xml
npm -v
```

```xml
git --version
```
![这样的](https://img-blog.csdnimg.cn/20210130142126915.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)
如果没出现如上的可以查看[解决方案](https://blog.csdn.net/qq_51644623/article/details/113276833)          
    [解决方案](https://blog.csdn.net/qq_51644623/article/details/113270377)
 然后输入

```xml
 npm install hexo-cli -g
```
![hexo的下载](https://img-blog.csdnimg.cn/20210130142523248.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)
出现+hexo-cli@4.2.0代表成功了（注意有的版本会不一样）

## 三：将hexo与GitHub连接
然后在任意盘新建**一个  空的  文件夹**，在此文件夹，右键git bash here
输入hexo init开始初始化

```xml
hexo init
```
![初始化](https://img-blog.csdnimg.cn/20210130142832577.png)

稍等一下，当出现start bloging with hexo代表初始化成功
然后安装依赖性文件，输入npm install

```xml
nom install
```
![下载](https://img-blog.csdnimg.cn/2021013014292994.png)
安装成功后
 安装部署插件，输入
```xml
npm install hexo-deployer-git --save
```

配置git个人信息，生产新的ssh密钥

```xml
git config --global user.email "you@example.com"
```

//注册github用的邮箱

```xml
git config --global user.name "yourname"
```
 //github用户名

打开Git Bash（桌面上鼠标右击 Git Bash here）输入
```xml
ssh‐keygen ‐t rsa ‐C "your_email@example.com"
```
然后一直点回车，最后完成后会在用户主目录下（C:\Users\用户名）生成.ssh目录，里面有id_rsa.pub文件。id_rsa_pub是公钥，复制其内容然后登陆github，打开seetings ——>SSH and GPG keys ，点击new SSH key，填上任意title，在key文本框里粘贴刚才复制的内容，点击Add SSH Key。
```xml
hexo g -d
```

然后输入

```xml
hexo s
```

就会在本地给你开启locahost:4000的端口

```xml
hexo 4000
```

![4000](https://img-blog.csdnimg.cn/20210130143006946.png)
[如果打不开可能窗口被占，点击查看如何解决](https://blog.csdn.net/buppt/article/details/78949315)
打开后的样子
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210130143250274.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

然后开始设置让这个本地端口让别人访问，用到github账号，在部署到远端访问前，要下载一个deployer的插件，
输入npm install hexo-deployer-git --save

```xml
npm install hexo-deployer-git --save
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210130143500712.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)

到原来的新建文件夹里找到_config.yml文件
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210130143645560.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210130143653362.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210130143714149.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)
最后有个deploy，把type类型写成git，除了type，还要加上repo和branch，repo就是在GitHub上的网址，branch填主分支msater，注意这两个在填写时前边必须有空格，修改好后按ctrl+s保存
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210130143742210.png)
返回命令行

```xml
hexo clean
```
```xml
hexo g -d
```
输入hexo g -d开始推送到GitHub


## 四：博客主题更换
[博客主题设置](https://blog.csdn.net/yaluoshan/article/details/80630653?ops_request_misc=%25257B%252522request%25255Fid%252522%25253A%252522161189561816780265410982%252522%25252C%252522scm%252522%25253A%25252220140713.130102334..%252522%25257D&request_id=161189561816780265410982&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-80630653.first_rank_v2_pc_rank_v29&utm_term=hexo%25E6%258D%25A2%25E4%25B8%25BB%25E9%25A2%2598)
## 五：电脑更换系统或更换电脑博客的重新部署
**一：要拷贝下来的重要内容**
1 _config.yml:站点配置文件
2 theme:主题文件
3 source：这个肯定是要拷贝，里面有写的博客文件
下边的可以不用：
4 scaffolds：文章模板
5 package.json：说明使用哪些包
6 .gitignore：限定在提交的时候哪些文件可以忽略
**二：开始部署**
先下载“Git”，和“node.js”
在你拷贝的文件夹里新建一个文件夹，在文件夹里打开git bash here

依次输入
```xml
 npm install hexo-cli -g
```
![hexo的下载](https://img-blog.csdnimg.cn/20210130142523248.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxNjQ0NjIz,size_16,color_FFFFFF,t_70)
出现+hexo-cli@4.2.0代表成功了（注意有的版本会不一样）

```xml
hexo init
```

```xml
npm install
```
**然后将拷贝的文件让新生成的文件覆盖**
安装成功后
 安装部署插件，输入
```xml
npm install hexo-deployer-git --save
```

配置git个人信息，生产新的ssh密钥

```xml
git config --global user.email "you@example.com"
```

//注册github用的邮箱

```xml
git config --global user.name "yourname"
```
 //github用户名

打开Git Bash（桌面上鼠标右击 Git Bash here）输入
```xml
ssh‐keygen ‐t rsa ‐C "your_email@example.com"
```
然后一直点回车，最后完成后会在用户主目录下（C:\Users\用户名）生成.ssh目录，里面有id_rsa.pub文件。id_rsa_pub是公钥，复制其内容然后登陆github，打开seetings ——>SSH and GPG keys ，点击new SSH key，填上任意title，在key文本框里粘贴刚才复制的内容，点击Add SSH Key。
```xml
hexo g -d
```
在输入

```xml
hexo s
```
查看是否成功。
## 六：目录设置及调整
修改next主题的ejs文件
我们首先要编辑文章显示页面的模板，也就是`themes/next/layout/_partial/article.ejs`文件。为了将目录生成在正文之前，我们首先在这个文件中找到`<%- post.content %>`，并在这一行之前加入如下代码：
```xml
<!-- Table of Contents -->
<% if (!index && post.toc){ %>
  <div id="toc" class="toc-article">
    <strong class="toc-title">文章目录</strong>
    <%- toc(post.content) %>
  </div>
<% } %>
```
这段代码的含义清晰明了，if语句中有两个条件，!index是为了不在首页的文章摘要中生成目录，post.toc确保了只在显式地标记了`toc: true`的文章中生成目录。若这两个条件满足，则创建一个目录的<div>。

修改完这个文件之后，找一篇包含了多个子标题的文章，并在文章开头的front-matter中添加一句toc: true，在浏览器中访问这篇文章，应该可以看到文章的开头处已经有了带链接的目录。但是这样的目录实在太难看，我们还需要添加相应的CSS来将其指定为我们想要的样式。
为目录编写CSS文件
要指定目录的样式，我们要修改的文件是`themes/next/source/css/_partial/article.styl`。在文件的最后，添加如下代码：

```xml
/*toc*/
.toc-article
  background #eee
  border 1px solid #bbb
  border-radius 10px
  margin 1.5em 0 0.3em 1.5em
  padding 1.2em 1em 0 1em
  max-width 28%
.toc-title
  font-size 120%
#toc
  line-height 1em
  font-size 0.9em
  float right
  .toc
    padding 0
    margin 1em
    line-height 1.8em
    li
      list-style-type none
  .toc-child 
    margin-left 1em
```

第一段的toc-article指定了目录整个<div>的背景色、边框色、倒角半径、各种间距以及最大的宽度。注意这里最好指定目录的最大宽度，我将其设为了28%，也就是文章正文那个框的宽度的28%，也可以设为一个固定的长度，比如在笔记本电脑上16em就是个不错的宽度，但为了能适配各种不同尺寸的屏幕，最好还是设置为百分比。如果不指定最大宽度，遇到比较长的标题时，生成的目录会非常难看。这个最大宽度的设置是我在网上其他添加目录的方法中没有见到的。
第二段的toc-title指的就是“文章目录”那四个字，这四个字要比其他字大一些，将其字号设为其他字的120%。
第三段的#toc.toc指定了目录列表的一些细节，将font-size设为0.9em会让目录的字比文章的字稍小一些。最后的.toc-child指定了二级目录的缩进量。
再次生成页面，应该已经可以显示比较美观的目录了。
**六选自[大佬链接](http://kuangqi.me/tricks/enable-table-of-contents-on-hexo/#%E4%BF%AE%E6%94%B9Landscape%E4%B8%BB%E9%A2%98%E7%9A%84ejs%E6%96%87%E4%BB%B6)**
经另一个大佬指导最后改成这个

```xml
/*toc*/
.toc-article
  background #eee
  border 1px solid #bbb
  border-radius 10px
  margin 1.5em 0 0.3em 1.5em
  padding 1.2em 1em 0 1em
  max-width 28%
.toc-title
  font-size 120%
#toc
  line-height 1em
  font-size 0.9em
  position fixed
  right 10px
  .toc
    padding 0
    margin 1em
    line-height 1.8em
    li
      list-style-type none
  .toc-child 
    margin-left 1em
```
## 七：这个博客的一些操作
1.用 markdown写文章时插入<!--more-->,文章会自动从插入的位置截断，也就是说在博客中只显示<!--more-->之前的内容，点击阅读全文之后会显示所有内容。
2.标记toc: true的文章中生成目录
3.标记toc: true置顶
