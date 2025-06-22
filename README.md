大家好，我是NAS区最帅的up主星灵技术，很高兴再次与大家见面，这里先讲述一下做这个系列视频的目的，因为我发现一个现状那就是网络上现在有很多论坛很多大佬博客也有很多教学视频但是这些技术相关的视频都过于分散了，而技术的理解往往需要一定的基础，如果是一个没有任何经验的网络小白的话，他是很难从零开始克服一个个技术难关的，所以我打算做这一系列视频让大家从零开始逐步深入了解NAS圈的全部。这样如果你再看大佬的github项目可能就可以轻松秒杀了。

今天我们将从无服务器无NAS的白嫖开始，好的，让我们正式开始NAS教程cloudflare篇。
首先，老手可以直接去看博客或者其他平台的图文教程，具体链接在评论区置顶。

### 本期教程的伟大之处在于一次性带你白嫖cloudflare部署六个项目，所有需求一步到位。分别是影视，新闻聚合，机场，github代理，docker代理还有个人图床。
提到cloudflare，我们所需要做的第一件事就是去购买一个域名，强烈前往name.com购买一个以xyz结尾的域名，具体教程如下：
前往如下链接：[Name.com | Domain Names, Registration, Websites & Hosting](https://www.name.com/zh-cn)
可以使用国内的支付宝进行购买，一年只需要几元钱十分划算。
我个人不建议使用免费域名，如果你一定要用免费域名，可以去网上自行搜索。
当你购买了一个域名，比如：example.xyz。
下面让我们开始把域名绑定cloudflare账号。
前往如下链接：https://dash.cloudflare.com/ 正常进行账号注册。应该会看到如下页面：
![](https://201014.xyz/docs/1749991184902.png)
接下来点击“域注册”，填入你的域名并进行搜索，应该会弹出一个对应的窗口，删掉对应的dns记录，然后应该会显示一个叫做“nameservers"的东西，将这两个nameservers进行复制。
如果你在这一块遇到了问题，也可以在b站查看其他视频，因为这一块非常简单所以我会讲的比较快。
回到先前的地址：https://www.name.com/zh-cn
点击我的域名或者my domains.
![](https://201014.xyz/docs/1749991540640.png)

点进你的域名应该会看到如下：
![](https://201014.xyz/docs/1749991612492.png)
然后继续找到域名服务器
应该会看到如下：
![](https://201014.xyz/docs/1749991717615.png)
这里一定要先删除原有的两个默认的，然后添加上两个cloudflare的并且保存。
这样等待几分钟或者几小时，再返回cloudflare地址应该就会显示你的域名了。


### 我们就可以开始今天的教程：
### 首先影视在线观看项目：libretv。
首先点击如下链接： [LibreSpark/LibreTV: 一分钟搭建影视站，支持Vercel/Docker等部署方式](https://github.com/LibreSpark/LibreTV)
![](https://201014.xyz/docs/1749992314110.png)

让我们回到cloudflare: https://dash.cloudflare.com/
点击workers按钮：
![](https://201014.xyz/docs/1749992427469.png)
然后点击创建，选择Pages中导入github:
![](https://201014.xyz/docs/1749992475027.png)
选择libretv项目：
![](https://201014.xyz/docs/1749992560753.png)
然后点击开始设置，注意这里需要设置一个密码：
![](https://201014.xyz/docs/1749992626560.png)
然后部署即可。
部署完了以后点击这个项目进行管理：
![](https://201014.xyz/docs/1749992701189.png)

设置自己的自定义域名：
![](https://201014.xyz/docs/1749992752480.png)
这里只需要填入libre.example.xyz即可，其中example.xyz是你自己购买的域名。
然后打开浏览器，访问https://libre.example.xyz,输入你自己设置的PASSWORD即可进入应用。
![](https://201014.xyz/docs/1749992859725.png)

好了这样我们今天的第一个教程，部署影视在线观看项目就结束了。
下一集我们将进行新闻聚合项目的部署，该项目汇总全网新闻总结在一个网页供你访问。
如果你喜欢本视频的话，欢迎一键三连，也希望大家可以去其他平台看看我发的博文，我们下集再见。

### 全网新闻聚合：Newsnow项目部署教程
其实这和上一个项目的部署方式极其相似，看过上一期视频的朋友们如果具备一定归纳总结能力的话，那么这个教程就会写的比较简单。所以就不放具体的图片了。

首先打开github链接： [ourongxing/newsnow: Elegant reading of real-time and hottest news](https://github.com/ourongxing/newsnow)
然后fork，然后前往cloudflare创建pages选择newsnow，不需要添加密码，直接保存并部署，填入自定义域名就可以访问了。
![](https://201014.xyz/docs/1749993256769.png)
怎么样是不是十分简单？

