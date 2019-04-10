---
description: 允许用户从单个页面布局和URL点进集合。
seo-description: 允许用户从单个页面布局和URL点进集合。
seo-title: Change Collection
solution: Experience Manager
title: Change Collection
uuid: 69bafcc7-c55 e-47d6-bc79-b0 db80 fdf138
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Change Collection{#change-collection}

允许用户从单个页面布局和URL点进集合。

使用Change Collection委托更改页面上显示的集合，而无需更改URL，而Livefyre应用程序已加载。使用此功能可显示照片画廊或视频画廊，或其他应用程序(在用户操作后显示的集合应更改)。

例如，单击画廊中的视频或照片将加载特定于该选择的集合，而页面的URL不会更改。

从 [单个注释计数](/help/implementation/c-advanced-topics/t-display-comment-count.md) 页面加载三个收藏集之一：

```
<html> 
<head> 
<script src='//cdn.livefyre.com/Livefyre.js'></script> 
</head> 
<body> 
<script type="text/javascript"> 
convConfig1 = {"collectionMeta": <COLLECTION META 1>, 
             "checksum": <CHECKSUM 1>, 
             "siteId": <SITE ID>, 
             "articleId":"1", 
             "el":"livefyre"}; 
convConfig2 = {"collectionMeta": <COLLECTION META 2>, 
             "checksum": <CHECKSUM 2>, 
             "siteId": <SITE ID>, 
             "articleId":"2", 
             "el":"livefyre"}; 
convConfig3 = {"collectionMeta": <COLLECTION META 3>, 
             "checksum": <CHECKSUM 3>, 
             "siteId": <SITE ID>, 
             "articleId":"3", 
             "el":"livefyre"}; 
  
Livefyre.require(['fyre.conv#prod'],function(Conv) { 
    new Conv({"network": "<NETWORK NAME>"}, 
    [convConfig1], 
    function(app) {  
        window.changeConv = app.changeCollection; 
    } 
    ); 
}); 
</script> 
  
<div id="livefyre"></div> 
<button onclick="window.changeConv(convConfig1);">Conv 1</button> 
<button onclick="window.changeConv(convConfig2);">Conv 2</button> 
<button onclick="window.changeConv(convConfig3);">Conv 3</button> 
</body> 
</html>
```
