---
description: 通过遵循类似于核心应用程序的过程来集成Sidesorp应用程序。
seo-description: 通过遵循类似于核心应用程序的过程来集成Sidesorp应用程序。
seo-title: Sides表示集成
solution: Experience Manager
title: Sides表示集成
uuid: 4aa14ada-402a-482d-b43e-96f37afa6c53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff

---


# Sides表示集成{#sidenotes-integration}

通过遵循类似于核心应用程序的过程来集成Sidesorp应用程序。

一般而言，如果您的核心应用程序集成完成，为生成对象而编写的代码可 `collectionMeta` 能会重用于Sidestraf。

您还可以通过在（可选）字 `auth` 段中向Siderav创建的委 `auth` 托来重 `fyre.conv` 复使用现有委托 `authDelegate` 。

>[!NOTE]
>
>Sidesform允许您在单 `network`个对象 `siteId`中包 `articleId` 含、和，而不是分别传递给构造函数的其他部分。

```
<!DOCTYPE html> 
<html> 
<head> 
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
</head> 
<body> 
<script type="text/javascript"> 
var convConfig = { 
 network: 'client-solutions.fyre.co', 
 selectors:'span.lyrics-sidenote', 
 siteId: '356373', 
 articleId: 'sidenotes-sample', 
 collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5zaWRlbm90ZXMtZGVtby5jb20vbHlyaWNzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAidHlwZSI6ICJzaWRlbm90ZXMiLCAiYXJ0aWNsZUlkIjogInNpZGVub3Rlc19zYW1wbGUiLCAidGl0bGUiOiAiQ2xpZW50IFNvbHV0aW9ucyBTaWRlbm90ZXMifQ.2gxnsM0TS8dfp-Jokb5uW1kuMl-DqIlqfJSCBwJgf1k' 
}; 
  
Livefyre.require(['sidenotes#1', 'auth'], function (Sidenotes, Auth) { 
 new Sidenotes(convConfig); 
 Auth.delegate({ 
 login: function (callback) { 
 callback(null,{livefyre:'<userauthtoken>'}); 
 } 
 }); 
 }); 
</script> 
</body> 
</html>
```

正如“构建”部分 `collectionMeta` 所述， `collectionMeta` 它是一个编码JSON对象。 在上面的示例中，JSON对象在进行JWT编码之前采用以下格式。

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

有关详细信息，请参阅 `collectionMeta` 令牌。

## 移动设置

Sidesk已针对在移动设备中的使用进行了优化。 为获得Livefyre应用程序的移动版本的最佳效果，请将用户可缩放选项设置为no。 例如：

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
