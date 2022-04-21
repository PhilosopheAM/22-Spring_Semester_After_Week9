# Introduction to softwares used in building & running a server 用于搭建服务器的软件介绍

This chapter is produced based on the lecture given by **CodeSheep** in bilibili. Follow this video:
> https://www.bilibili.com/video/BV1ra4y1t7rs?share_source=copy_web

## 服务器的硬件部分 
略。唯一要注意的点是，有更多的中小型企业上云。可以注意一下云服务的发展。

## 静态与动态
很好的例子是许多广泛应用的博客框架
+ 静态 - Hexo
+ 动态 - Halo
+ 动态 - WordPress
像Halo WordPress这样的有后台应用服务的托管博客需要单独的应用服务器的承载，部署起来会更加麻烦（提供的功能也更有趣）

## 三种服务器
+ Web服务器
+ HTTP服务器
+ 应用服务器
  
Web服务器就是用于响应用户需求，按需（设计功能）提供Web化服务（比如说邮件服务、视频流上下行）. 需要注意的是，在协议通讯层许多服务都是使用HTTP协议，所以Web服务器与HTTP服务器不用做严肃区分。  
当然，HTTP服务器将服务器上的资源通过HTTP协议形式传输给客户端，我们强调这个过程对静态资源传输的支持，所以有时候也叫它静态服务器。  
对于应用服务器，字面意思就是一个特定应用的承载容器。一个应用嘛，一般来说就需要运行时环境支持(environment). 比如Java下的Tomcat.应用服务器可以生成动态的资源提供给客户端（动态响应），所以我们也称它为“动态容器”、“Web容器”、“动态服务器”、“应用容器”.

## 不同服务器软件介绍

|Software|Type|Description|Application|Advantage|Other|
|:---|:---|:---|
|Nginx|HTTP服务器|将静态资源通过HTTP协议传输给客户端；现在一般用它来做**反向代理服务器**或者**负载均衡**|现实应用中一般用Nginx作为客户端-后端真正的动态服务器之间的配合，做服务请求转发，提供灵活稳定的Web服务|性能好，稳定性高，内存消耗少|纯C语言，开源；大量企业使用Nginx|
|Tengine|HTTP服务器|基于Nginx做的改版，阿里开发|主要面向大流量场景，比方说淘宝|大规模检验，稳定性好|Null|
|Apache HTTP Server|HTTP服务器|和Nginx功能相像，但并发性、负载、资源消耗方面比不上Nginx|最近大家转向Nginx较多|Null|Apache基金会项目，开源|
|IIS|Web服务|是一个HTTP静态服务器，但是支持ASP.NET，所以可以作为Web服务器使用|因为是Windows生态的，很少用|Null|Windows开发，不开源|
|Tomcat|Java应用服务器软件|Java runtime下做Java EE的应用服务器|SpringBoot将Tomcat作为内嵌的默认应用服务器（容器）；在流量不大的情况下可以直接做HTTP服务器用（一般不会用，不会让Tomcat直面用户）|名声响啊|Apache软件基金会项目|
|Jetty|






