---
description: 将用户内容绘制到交互式地图。
seo-description: 将用户内容绘制到交互式地图。
seo-title: 地图
solution: Experience Manager
title: 地图
uuid: 1c399d-a610-4b80-a3 b2-a5502 b31480 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 地图{#map}

将用户内容绘制到交互式地图。

地图允许您将地理围栏内容流式传输到世界地图上，以便在突发新闻或实时活动周围找到社交缺陷。将显示所有适用的内容，包括文本、注释、照片和帖子。

>[!NOTE]
>
>地图由 [© OpenStreetMap](https://www.openstreetmap.org/copyright)提供支持，它提供Livefyre用于渲染其映射的数据。

## 集成 {#section_w2m_db2_d1b}

使用地图最快的方法是使用Livefyre的CDN上托管的版本。

首先，将 [Livefyre. js](https://github.com/Livefyre/Livefyre.js) 添加到您的页面。

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

然后，定位将显示地图应用程序的元素。

```
<div id="map" style="height: 500px;"></div>
```

最后，使用Livefyre构建映射，并从streub-sdk中获取要管道的集合。请记住，映射只能显示具有地理网格元数据的内容。Twitter和Instagram特选支持此功能。为确保最佳性能，请在您的集合的所有Currate规则上加入地理位置过滤器。

```
<script> 
Livefyre.require(['streamhub-map#1', 'streamhub-sdk#2'], 
function (Map, SDK) { 
    var map = new Map({ 
        el: document.getElementById('map') 
    }); 
    var collection = new SDK.Collection({ 
        network: 'strategy-prod.fyre.co', 
        siteId: 340628, 
        articleId: 'custom-1389845009515' 
    }); 
    collection.pipe(map); 
}); 
</script>
```

查看此 [实时示例](https://codepen.io/cheung31/pen/wkmbF)。

## 配置 {#section_jc5_gxb_c1b}

`initial`

从集合加载并显示在地图上的初始项目数。加载此号码后，用户可以单击按钮以显示更多内容。(可选)。默认为50。)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

传递到底层 [Leaflet](https://leafletjs.com/) 地图的选项，映射用于渲染。使用此选项可设置 [“Leaflet映射选项](https://leafletjs.com/reference.html#map-options)”，包括地图的初始中心点以及初始和最大缩放级别。(可选。)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

