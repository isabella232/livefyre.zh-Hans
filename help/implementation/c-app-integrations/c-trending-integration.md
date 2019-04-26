---
description: 在您的网站或网络上展示最活跃的收藏集。
seo-description: 在您的网站或网络上展示最活跃的收藏集。
seo-title: 趋势趋势
solution: Experience Manager
title: 趋势趋势
uuid: 3031523d-b487-4ea-bba6-5d8 f9971874 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 趋势趋势{#trending}

在您的网站或网络上展示最活跃的收藏集。

使用趋势来展示集合在站点或网络中的最新活动。

## 集成 {#section_wtz_whb_c1b}

与Trending集成的最快捷方法是使用Livefyre的CDN上托管的版本。

首先，将 [Livefyre. js](https://github.com/Livefyre/Livefyre.js) 添加到您的页面。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

然后，定位将显示应用程序的元素。

```
<div id="trending"></div>
```

最后，使用 `Livefyre.require` 构造组件。

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

您现在有一个趋势应用程序！查看 [此示例](https://codepen.io/gobengo/pen/GijEy)中的所有操作。

## 配置 {#section_k5k_qhb_c1b}

`network`

将从中提取集合的网络。(必需。)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

提供站点ID，以便仅从网络中的单个站点显示集合。(可选。)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

提供一个集合标签，以仅显示带该标记的集合。(可选。)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

