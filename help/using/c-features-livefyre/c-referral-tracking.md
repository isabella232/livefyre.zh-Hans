---
description: 跟踪从引用流量返回到您的页面的点击量。
seo-description: 跟踪从引用流量返回到您的页面的点击量。
seo-title: 引用跟踪
solution: Experience Manager
title: 引用跟踪
uuid: 7daf615d-0c07-49d1-adb2-1ac67 ea563 e7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 引用跟踪{#referral-tracking}

跟踪从引用流量返回到您的页面的点击量。

在发布或共享评论至社交网络以及Livefyre电子邮件中包含的恶意链接时，Livefyre会向URL附加引用变量。使用此变量可跟踪从Livefyre Apps到您的社交或自有资产的引用流量。

Livefyre Apps允许您跟踪由引用流量产生的数据流，从而分析站点流量。

## 跟踪Livefyre引用流量 {#section_nsy_qp4_xz}

通过检查页面URL中的查询字符串参数和在页面上实施代码，可跟踪来自社交网络和电子邮件的Livefyre引用流量，以便通过您的分析提供商跟踪此情况。在发布或共享评论到社交网络以及Livefyre电子邮件中包含的恶意链接时，Livefyre会附加指向URL的引用链接。

## 实施示例 {#section_xvs_x44_xz}

如果流量来自StreamHub驱动的通知，将有一个HubeBrfsc查询字符串参数，该参数具有电子邮件、Facebook、Twitter、LinkedIn或malmalink值。HubeBrimsc参数名称可由Livefyre交付团队在网络级别进行配置。

要与分析平台集成，您的页面必须在加载时查找HubeBrfsc，如果存在，则记录流量。

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

* [聊天](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [注释](/help/using/c-about-apps/c-comments/c-comments.md)
* [评论](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Siten表示](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

