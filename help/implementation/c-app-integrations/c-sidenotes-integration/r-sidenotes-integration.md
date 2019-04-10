---
description: 按照类似于核心应用程序的流程集成SiteNote应用程序。
seo-description: 按照类似于核心应用程序的流程集成SiteNote应用程序。
seo-title: Sitenes集成
solution: Experience Manager
title: Sitenes集成
uuid: 4aa14a-402a-482d-b43 e-96f37 afa6 c53
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sitenes集成{#sidenotes-integration}

按照类似于核心应用程序的流程集成SiteNote应用程序。

一般而言，如果核心应用程序集成已完成，则为生成 `collectionMeta` 对象而编写的代码可能会被重复使用为SiteNote。

您还可以通过在(可选 `auth` )字段中向SiteNote提供创建 `auth` 的委托 `fyre.conv` 来重复使用 `authDelegate` 现有委托。

>[!NOTE]
>
>Siten表示允许您包括 `network`和 `siteId``articleId` 在单个对象中，而不是在构造函数的其他部分单独传递它们。

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

如构建 `collectionMeta` 部分中所述， `collectionMeta` 是一个编码的JSON对象。在上面的示例中，JSON对象在JWT编码之前采用以下格式。

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

有关更多信息，请参阅 `collectionMeta` 令牌。

## 移动设置

Sitenks已经过优化，可在移动设备中使用。为获得使用Livefyre应用程序的移动版本的最佳效果，请将用户可升级选项设置为no。例如：

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
