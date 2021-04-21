---
description: 通过遵循类似于核心应用程序的流程来集成Siserapp。
title: Sidesr集成
exl-id: 368951b1-fef2-46d8-b89c-68c46962e937
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---

# Siestrator集成{#sidenotes-integration}

通过遵循类似于核心应用程序的流程来集成Siserapp。

通常，如果您的核心应用程序集成完成，则为生成`collectionMeta`对象而编写的代码可能会重用于Siestrator。

您还可以通过在（可选）`authDelegate`字段中将使用`fyre.conv`创建的`auth`委托提供给Siestr来重复使用现有`auth`委托。

>[!NOTE]
>
>Siestar允许您将`network`、`siteId`和`articleId`包含在单个对象中，而不是在构造函数的其他部分中单独传递它们。

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

如构建`collectionMeta`部分中所述，`collectionMeta`是编码的JSON对象。 在上面的示例中，JSON对象在进行JWT编码前采用以下格式。

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

有关详细信息，请参阅`collectionMeta`令牌。

## 移动设置

Siters已针对移动设备进行优化。 为获得移动版Livefyre应用程序的最佳效果，请将用户可缩放的选项设置为no。 例如：

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
