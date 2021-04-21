---
description: 允许用户从单个页面布局和URL中点击浏览集合。
title: 更改收藏集
exl-id: 5cfae2c6-e328-4d2c-b08b-709be94e4c54
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# 更改集合{#change-collection}

允许用户从单个页面布局和URL中点击浏览集合。

在已加载Livefyre应用程序时，使用更改集合委派来更改页面上显示的集合，而不更改URL。 使用此功能可显示照片或视频画廊，或用户操作后显示的收藏夹应发生更改的其他应用程序。

例如，单击画廊中的视频或照片将加载特定于该选择的收藏集，而页面的URL不会更改。

要从单个[注释计数](/help/implementation/c-advanced-topics/t-display-comment-count.md)页加载三个集合中的一个：

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
