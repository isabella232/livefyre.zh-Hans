---
description: 从引用流量跟踪点击回您的页面。
title: 推荐跟踪
exl-id: 9955d4a4-184d-421f-bcde-b19342b0b181
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 2%

---

# 引用跟踪{#referral-tracking}

从引用流量跟踪点击回您的页面。

当将评论发布或共享到社交网络时，Livefyre会向URL附加一个引用变量，并针对Livefyre电子邮件中包含的超链接添加该变量。 使用此变量跟踪从Livefyre Apps到您的社交或所有属性的引用流量。

Livefyre应用程序允许您跟踪由引用流量产生的数据流，从而使您能够分析您网站的流量。

## 跟踪Livefyre转诊流量{#section_nsy_qp4_xz}

可以通过检查页面URL中的查询字符串参数，并在页面上实施代码来跟踪来自社交网络和电子邮件的Livefyre引用流量，以跟踪这些流量。 在将评论发布或共享到社交网络时，Livefyre会为包含在Livefyre电子邮件中的访客添加一个指向该URL的引用链接。

## 实施示例 {#section_xvs_x44_xz}

如果流量来自由StreamHub提供的通知，则将有一个hubRefSrc查询字符串参数，其值为email、facebook、twitter、linkedin或permalink。 您的Livefyre投放团队可以在网络级别配置hubRefSrc参数名称。

要与分析平台集成，页面必须在加载时查找hubRefSrc，并记录存在的流量。

例如：

```
(function () { 
   var qs = document.location.search.substring(1), 
      param = 'hubRefSrc', 
      valueRegex = new RegExp(param+'=([^&]+)'), 
      match = qs.match(valueRegex), 
      referrer; 
   if (match) { 
      // StreamHub generated traffic! 
      referrer = match[1]; 
      console.log('StreamHub referred via', referrer); 
   } else { 
      // StreamHub did not refer this traffic 
   } 
}())
```

使用此功能的应用程序：

* [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md)
* [评论](/help/using/c-about-apps/c-comments/c-comments.md)
* [评论](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md)
* [Siestr](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)
