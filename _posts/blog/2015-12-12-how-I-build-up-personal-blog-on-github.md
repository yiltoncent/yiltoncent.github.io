---
layout: post
title:  我在github上建立个人博客的过程
description: Github的其他的服务，比如Github Pages，使用它可以很方便的建立自己的独立博客，并且免费。
category:    blog
---



# 背景
进一年前其实我就有建立个人博客的想法，那时候看到阮一峰老师的[一篇博文:搭建一个免费的，无限流量的Blog----github Pages和Jekyll入门](http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html)。当时兴致勃勃的想搞一个自己博客出来，也努力尝试了，只不过当时是在水平有限，相关知识结构短缺，也未能搞出个模样。最终就是照着阮老师的博客搭了一个`你好，世界`的简易页面出来，接着在CSDN上写了一篇博客：[如何使用Jekyll在github上搭建一个blog ](http://blog.csdn.net/wuxianglonghaohao/article/details/42655499)。

事物的客观规律就是这样，当你想做成一件事情，而相关知识结构几乎为零，那么你一次性做成的可能性为零。但是一年来的工作学习，多多少少积攒起来，对建立一个博客开始有系统性、全面性的理解了。忘记说了，我目前的工作是做嵌入式开发，对于网络、网页这块的认识相对缺乏。所以在别人开来很简单的一些概念对我来说都是需要学习的。

# 建立博客过程

长久以来都想有一个自己的域名，有一个自己的博客，写点什么放上去，既可以给别人看看提供参考，也能方便自己回忆某些知识点。所以就写作而言，不仅是分享，也是一种整理自己思路、连接相关知识点的行为，利人利己。

建立过程可以分两部分：一部分是跟域名相关的，这部分我跟BeiYuu的博客描述有些差异，关于域名解析也发生了变化，我会一一解释；另一部分是跟博客即github相关的，我几乎就是将他的fork过来，然后做了一些个人信息的修改。

建立博客参考的就是这两篇博文：<[我为什么写博客？](http://beiyuu.com/why-blog/)>以及<[使用Github Pages建独立博客](http://beiyuu.com/github-pages/)>。前一篇文章有点像武林秘籍中的理论篇，中心点就是：`生命在于折腾`，这也跟我性格很符合；后一篇就是武林秘籍中的招式图解，一步步教会你怎么搞出来。

## 购买域名
在看到这两篇博客之前，我也搜索了很多相关的博客，从如何购买域名，如何注册域名解析，到如何使用github以及git,对大概过程有个了解。

与BeiYuu不同，我的域名[yiltoncent.com](yiltoncent.com)不是在Godaddy上买的，我同事推荐我在namesilo上购买，算下来确实要便宜点。购买了5年的域名注册，网上搜了一个一美元的优惠码，总共是43.5美元搞定。

如果大家想购买域名，建议大家在namesilo上购买，原因有以下两点：

* 相对godaddy，namesilo的总价格要便宜一点，虽然godaddy经常搞各种优惠码，但是算下来还是贵上小十美元。最重要的是，省去你去满天下找优惠码的烦恼，优惠码只有一个，一美元的优惠，很好找。
* 相对godaddy，namesilo提供whois永久免费的隐私保护，前者是收费的。隐私保护我觉得还是蛮重要的。

另外提醒一点，namesilo是可以用支付宝付款的，也可以用信用卡付款，当然至少是双币的。

## 域名解析
域名解析这一块刚开始可把我搞糊涂了，很多文章都提到要注册DNSPOD，然后添加记录，有些文章中提到在namesilo里面要设置nameserver以及A记录、CNAME记录等。对于我这小白来说，根本搞不清楚，可能在他们看来这是最简单不过的事情，根本没想到要解释一下。这儿我来解释一下，其实购买完域名后，可以直接使用namesilo的域名解析服务器，如：`NS1.DNSOWL.COM`。但我们的博主们还是习惯用国内的域名解析服务器，可能跟国外的一些网站经常被GFW墙有关吧。假如你在不同的域名注册提供商那里注册了不同的域名，你在一家域名服务器提供商那里注册域名解析，更方便管理。所以这里搞清楚就好了。

所以我也使用了DNSPOD的域名解析：
![nameserver.png-47.6kB][1]

这里要注意一下，BeiYuu的博文提到：
![arecord.png-12.7kB][2]
这是不对的，github pages的这篇文章[My custom domain isn't working](https://help.github.com/articles/my-custom-domain-isn-t-working/)提到：
![dnserrors.png-71.5kB][3]
应该将`A`记录指向`192.30.252.153`和`192.30.252.154`。

另外，DNS生效过程真耗时间。OK，现在能ping通我的域名了。DNS解析已经完成。

## 博客移植
其实博客移植这一部分是最不需要讲述的，因为按照BeiYuu的方法直接做好，push到github上面就可以了。没有什么难度。这儿只介绍自己关心的两点：

* 修改个人信息，`_config.yaml`里面修改自己的域名以及ID;`_layouts/default.html`也有个人相关的信息一并改掉，这儿稍微注意一下个人联系方式：
![2015-12-12 01-29-27屏幕截图.png-23kB][4]
* 修改favicon.ico，这个就在网上找一下制作icon的网站，换成自己喜欢的icon即可。


# 总结
大概就这么多，总之，生命在于折腾。接下来就安静的谢谢文章，看看书；学习学习前端知识，在看到博客不满意的地方再修改修改。


  [1]: http://static.zybuluo.com/yiltoncent/s7f3vqa0hup5w1mw6aiqz3py/nameserver.png
  [2]: http://static.zybuluo.com/yiltoncent/urggtikfrgmtadz6dvwwjemq/arecord.png
  [3]: http://static.zybuluo.com/yiltoncent/xj80w4bkr92tio6pciwlo2pe/dnserrors.png
  [4]: http://static.zybuluo.com/yiltoncent/amv5kj12jp3hcfrpvt6xy6cs/2015-12-12%2001-29-27%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE.png
