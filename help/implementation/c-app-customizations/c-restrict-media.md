---
description: 限制进入应用程序流的媒体类型。
seo-description: 限制进入应用程序流的媒体类型。
seo-title: 限制媒体
solution: Experience Manager
title: 限制媒体
uuid: c470c985-d221-4f39-8bd4-4e44 ec14 db95
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 限制媒体{#restrict-media}

限制进入应用程序流的媒体类型。

默认情况下，所有媒体附件均可嵌入到应用程序中。Livefyre允许您更改此选项以防止用户将选定的附件类型发布到应用程序。

>[!NOTE]
>
>Livefyre合作伙伴与Embey合作，实现媒体集成。有关更多信息，请参阅内容集成>电子邮件无缝集成。有关链接扩展或源的问题，请与技术客户经理联系。

此示例阻止YouTube和Vimeo嵌入注释流：

```
var attachmentDelegate = function(embedObj) { 
   var providersToBlock = ['youtube', 'vimeo']; 
   for (var i=0, len=providersToBlock.length; i<len; i++) { 
      if (embedObj.provider_url.indexOf(providersToBlock[i]) > -1) { 
         return false; 
      } 
   } 
   return true; 
};
```

加载对话时：

```
networkConfig["attachmentDelegate"] = attachmentDelegate; 
fyre.conv.load(networkConfig, [convConfig]);
```

