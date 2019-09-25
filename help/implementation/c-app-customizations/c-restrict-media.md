---
description: 限制进入应用程序流的媒体类型。
seo-description: 限制进入应用程序流的媒体类型。
seo-title: 限制媒体
solution: Experience Manager
title: 限制媒体
uuid: c470c985-d221-4f39-8bd4-4e44ec14db95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 限制媒体{#restrict-media}

限制进入应用程序流的媒体类型。

默认情况下，所有媒体附件都可嵌入到应用程序中。 Livefyre允许您更改此选项，以阻止用户将选定的附件类型发布到您的应用程序。

>[!NOTE]
>
>Livefyre与Embedly合作实现媒体集成。 有关详细信息，请参阅内容集成&gt;嵌入式集成。 有关链接扩展或源的问题，请与您的技术客户经理联系。

此示例阻止YouTube和Vimeo从您的注释流中嵌入：

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

