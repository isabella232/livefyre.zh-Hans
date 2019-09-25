---
description: 允许用户从单个页面布局和URL中点进集合。
seo-description: 允许用户从单个页面布局和URL中点进集合。
seo-title: 更改集合
solution: Experience Manager
title: 更改集合
uuid: 69bafcc7-c55e-47d6-bc79-b0db80fdf138
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 更改集合{#change-collection}

允许用户从单个页面布局和URL中点进集合。

在Livefyre应用程序已加载时，使用更改集合委派来更改页面上显示的集合，而不更改URL。 使用此功能可显示照片或视频画廊，或显示的集合在用户操作后应更改的其他应用程序。

例如，单击画廊中的视频或照片将加载特定于该选择的集合，而页面的URL不会更改。

要从单个注释计数页面加载三个集合中的 [一个](/help/implementation/c-advanced-topics/t-display-comment-count.md) :

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

