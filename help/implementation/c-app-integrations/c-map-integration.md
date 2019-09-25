---
description: 将用户内容绘制到交互式地图。
seo-description: 将用户内容绘制到交互式地图。
seo-title: 地图
solution: Experience Manager
title: 地图
uuid: 1c3e399d-a610-4b80-a3b2-a5502b31480d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 地图{#map}

将用户内容绘制到交互式地图。

Map允许您将地理标记内容流化到世界地图上，从而定位突发新闻或实时活动周围的社交热点。 将显示所有适用的内容，包括文本、评论、照片和帖子。

>[!NOTE]
>
>地图由OpenStreetMap [提供支持](https://www.openstreetmap.org/copyright),Livefyre使用它来渲染其地图的数据。

## 集成 {#section_w2m_db2_d1b}

使用Map的最快捷方式是使用Livefyre的CDN上托管的构建版本。

首先，将 [Livefyre.js添加到您的页面](https://github.com/Livefyre/Livefyre.js) 。

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

然后，放置将在其中显示映射应用程序的元素。

```
<div id="map" style="height: 500px;"></div>
```

最后，使用Livefyre.require构建地图，并从streamhub-sdk中获取一个Collection以插入。 请记住，地图只能显示带有地理标记元数据的内容。 Twitter和Instagram Curate支持此功能。 要确保最佳性能，请在集合的所有“特定规则”上加入地理位置筛选器。

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

查看此实 [时示例](https://codepen.io/cheung31/pen/wkmbF)。

## 配置 {#section_jc5_gxb_c1b}

`initial`

要从集合加载并显示在地图上的项目的初始数量。 加载此编号后，用户可单击按钮以显示更多。 （可选。默认为50。)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

传递到底层宣传物料 [图的选项](https://leafletjs.com/) ,Map使用它进行渲染。 使用此选项可设置 [宣传物料地图选项](https://leafletjs.com/reference.html#map-options)，包括地图的初始中心点以及初始和最大缩放级别。 (可选.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

