---
description: 将用户内容绘制到交互式地图。
title: 地图
exl-id: 836b475e-0ec6-49f8-b89f-3af3209cf1f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 2%

---

# 地图{#map}

将用户内容绘制到交互式地图。

Map允许您将地理标记内容流化到世界地图上，从而定位有关突发新闻或实时事件的社交热点。 将显示所有适用的内容，包括文本、评论、照片和帖子。

>[!NOTE]
>
>地图由[© OpenStreetMap](https://www.openstreetmap.org/copyright)提供，后者提供Livefyre用于呈现其地图的数据。

## 集成 {#section_w2m_db2_d1b}

使用Map的最快捷方式是使用托管在Livefyre CDN上的构建版本。

首先，将[Livefyre.js](https://github.com/Livefyre/Livefyre.js)添加到您的页面。

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

然后，定位将在其中显示映射应用程序的元素。

```
<div id="map" style="height: 500px;"></div>
```

最后，使用Livefyre.require构建映射，并获取一个Collection以从streamhub-sdk进行插入。 请记住，地图只能显示带有地理标记元数据的内容。 Twitter和Instagram Curate支持此功能。 为确保最佳性能，请在您的集合的所有规则中加入地理位置筛选器。

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

查看此[实时示例](https://codepen.io/cheung31/pen/wkmbF)。

## 配置 {#section_jc5_gxb_c1b}

`initial`

要从集合加载并在地图上显示的初始项数。 加载此号码后，用户可以单击按钮以显示更多内容。 （可选。默认为50。)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

传递到基础[宣传物料](https://leafletjs.com/)映射的选项，Map用于渲染。 使用此选项可设置[宣传物料图选项](https://leafletjs.com/reference.html#map-options)，包括图的初始中心点以及初始和最大缩放级别。 (可选.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```
