---
description: 展示您网站或网络上最活跃的集合。
title: 趋势
exl-id: a3129e95-90e7-4107-bfd9-ed3b0dce20aa
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 5%

---

# 趋势{#trending}

展示您网站或网络上最活跃的集合。

使用趋势显示包含您网站或网络中最新活动的收藏集。

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

您现在有了Trending App! 在[此示例](https://codepen.io/gobengo/pen/GijEy)中查看所有操作情况。

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
