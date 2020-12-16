---
description: 展示您的站点或网络上最活跃的集合。
seo-description: 展示您的站点或网络上最活跃的集合。
seo-title: 趋势
solution: Experience Manager
title: 趋势
uuid: 3031523d-b487-4eea-bba6-5d8f9971874f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---


# 趋势{#trending}

展示您的站点或网络上最活跃的集合。

使用趋势显示包含网站或网络中最新活动的集合。

## 集成 {#section_wtz_whb_c1b}

与Trending集成的最快捷方式是使用托管在Livefyre CDN上的内置版本。

首先，将[Livefyre.js](https://github.com/Livefyre/Livefyre.js)添加到您的页面。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

然后，定位将在其中显示应用程序的元素。

```
<div id="trending"></div>
```

最后，使用`Livefyre.require`构建组件。

```
<script> 
Livefyre.require([ 
   'streamhub-hot-collections#0' 
], function(Trending) {     
   var app = new Trending({ 
      el: document.getElementById("trending"), 
      network: 'livefyre.com' 
   }); 
   app.start(); 
}); 
</script>
```

您现在有了热门应用！ 请参阅[此示例](https://codepen.io/gobengo/pen/GijEy)中的全部操作。

## 配置 {#section_k5k_qhb_c1b}

`network`

将从中提取集合的网络。 (必需.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

提供站点ID以仅显示网络中单个站点的集合。 (可选.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

提供单个“集合”标记以仅显示带有该标记的集合。 (可选.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

