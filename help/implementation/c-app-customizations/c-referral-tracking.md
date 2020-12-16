---
description: 从推荐流量跟踪点击回您的页面。
seo-description: 从推荐流量跟踪点击回您的页面。
seo-title: 推荐跟踪
solution: Experience Manager
title: 推荐跟踪
uuid: 5206cc16-9671-4b3d-a013-be1a3e8c029d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# 引用跟踪{#referral-tracking}

从推荐流量跟踪点击回您的页面。

在将评论发布或共享到社交网络时，Livefyre会向URL附加一个引用变量，并针对包含在Livefyre电子邮件中的永久链接添加该变量。 使用此变量跟踪从Livefyre应用程序到您的社交或自有资产的推荐流量。

Livefyre应用程序允许您跟踪由推荐流量产生的数据流，从而使您能够分析站点流量。

## 跟踪Livefyre引用流量{#section_nsy_qp4_xz}

可以通过检查页面URL中的查询字符串参数并在页面上实施代码来跟踪来自社交网络和电子邮件的Livefyre引用流量，以通过分析提供商来跟踪这些流量。 在将评论发布或共享到社交网络时，Livefyre会附加一个指向该URL的引用链接，并针对Livefyre电子邮件中包含的永久链接添加该链接。

## 实施示例 {#section_xvs_x44_xz}

如果流量来自由StreamHub驱动的通知，则将有一个hubRefSrc查询字符串参数，其值为email、facebook、twitter、linkedin或permalink。 hubRefSrc参数名称可由Livefyre投放团队在网络级别进行配置。

要与分析平台集成，页面在加载时必须查找hubRefSrc，并记录流量（如果存在）。

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
* [Sidesk](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)