---
description: 在单个页面上展示多个集合。
seo-description: 在单个页面上展示多个集合。
seo-title: 多个集合
solution: Experience Manager
title: 多个集合
uuid: 9675ffd7-1a59-42a1-b3ba-40af1744cfd1
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 1%

---


# 多个集合{#multiple-collections}

在单个页面上展示多个集合。

您可以在站点的单个页面上包含多个集合。 例如，要发布事件，您可能在事件期间有实时博客或聊天讨论，页面侧有单独的应用程序，显示社交Web周围的相关精选内容。 或者，您可以在文章下方加入评论应用程序，侧边可以聊天。

要在页面上获取多个对话，请在数组中添加一个或多个配置，然后将该数组传递给加载调用。 例如：

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
