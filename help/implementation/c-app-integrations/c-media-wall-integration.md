---
description: 通过实时内容流创建媒体墙。
seo-description: 通过实时内容流创建媒体墙。
seo-title: 媒体墙
solution: Experience Manager
title: 媒体墙
uuid: c6087c80-a35 b-44d2-9dd4-ba9 cd471172 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 媒体墙{#media-wall}

通过实时内容流创建媒体墙。

通过媒体墙，您可以为站点创建实时社交专区。使用Livefyre JavaScript SDK的streub-wall包将Livefyre社交源显示为一种视觉效果丰富、全屏、平铺的内容体验，这种体验非常适合涵盖实时活动、托管照片竞赛以及为网站的社交部分提供支持。

## 集成 {#section_jfm_bwb_c1b}

添加媒体墙最快捷的方法是使用Livefyre的CDN上托管的版本。

首先，将 [Livefyre. js](https://github.com/Livefyre/Livefyre.js) 添加到您的站点。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

然后，定位将显示媒体墙的元素。

```
<div id="wall"></div>
```

最后，使用 `Livefyre.require` 构造组件。

```
<script> 
Livefyre.require([ 
    'streamhub-wall#5' 
], function(MediaWall) {     
    var wall = window.wall = new MediaWall({ 
        el: document.getElementById("wall"), 
        collection: { 
            "network": "client-solutions.fyre.co", 
            "siteId": "364309", 
            "articleId": "answers-mediawall" 
        } 
    }); 
}); 
</script>
```

现在您有了墙！查看 [此示例](https://codepen.io/gobengo/pen/dFwDL)中的所有操作。

**点击错误？** 检查以确保传递正确的环境参数。选项包括 `livefyre.com` (生产)或 `t402.livefyre.com` (UAT)。

>[!NOTE]
>
>您的媒体墙应用程序渲染的帖子的任何样式自定义必须按照Twitter [的显示要求进行](https://dev.twitter.com/terms/display-requirements)操作。

## 配置选项 {#section_ucv_qvb_c1b}

`columns`

用于定义构造墙时媒体墙的列数。如果设置此选项，每个列的宽度将自动适应媒体墙的容器大小，同时保持指定的列数。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

在页面加载时呈现的内容项目数。默认为50。

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

允许您为媒体墙的容器元素中的每个列设置最小(像素)宽度。(您的媒体墙将根据容器元素的宽度自动选择适当的列数。默认情况下，媒体墙的宽度除以最低内容宽度(300px，如果未定义)确定列数。)

>[!NOTE]
>
>请勿与列选项结合使用此选项。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

默认情况下，当内容有附件时，媒体墙将显示可单击的缩略图。单击后，应用程序将打开一个模式，其中显示照片/视频附件全文。要禁用此选项，请将模态设置为false。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

定义 [!UICONTROL Post Content] 要显示在墙上的按钮。此选项需要传入，并向页面添加Livefyre. js `opts.collection`Auth集成。

`postButton` 参数：

* `false` (默认)：请勿显示帖子内容按钮。(创建只读媒体墙。)
* `true` (或 `LiveMediaWall.postButtons.contentWithPhotos`)：包含一个按钮，它允许用户添加文本内容和附加的照片。

* `LiveMediaWall.postButtons.content`：包含一个按钮，它允许用户添加文本内容，但不能附加照片。
* `LiveMediaWall.postButtons.photo`：包含允许用户添加照片但没有文本的按钮。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

定义单击 [!UICONTROL Show More] 按钮时要添加到墙中的内容项目数。

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## 样式配置选项 {#section_ztv_dvb_c1b}

媒体墙还提供若干配置选项，可用于自定义文本颜色、样式和大小。要实施这些选项，请使用以下语法：

```
var wall2 = window.wall2 = new MediaWall({ 
   el: document.getElementById("listView1"), 
   collection: collection, 
   cardBackgroundColor: '#333', 
   textColor: 'magenta', 
   linkColor: 'orange', 
   footerTextColor: 'lime', 
   displayNameColor: 'cyan', 
   usernameColor: 'red', 
   fontFamily: 'Helvetica, Arial', 
   linkAttachmentBackgroundColor: '#555', 
   linkAttachmentBorderColor: '#888' 
}); 
```

为获得有效的输入，请参阅W3C标准(CSS [字体系列](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family)、 [字体大小](https://www.w3.org/TR/CSS2/fonts.html#font-size-props)、 [线条高度和](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height)[颜色](https://www.w3.org/TR/css3-color/#colorunits) 属性)。

* **bodyfontSize***(CSS字体大小字符串)* 内容正文文本的字体大小。

* **bodyLineHeight***(CSS线高度字符串)* 内容正文文本的行高。

* **ButtonActiveBackgroundColor***(CSS颜色字符串)**活动时按钮背景的颜色。

* **ButtonBorderColor***(CSS颜色字符串)**按钮边框的颜色。

* **ButtonHovergroundColor***(CSS颜色字符串)* 悬停时按钮背景的颜色。

* **ButtonTextColor***(CSS颜色字符串)* 按钮标签的颜色。

* **cardBackgroundColor***(CSS颜色字符串)* 媒体墙中内容卡的背景颜色。

* **displayNameColor***(CSS颜色字符串)* 在署名中显示名称的颜色。

* **fontFamily***(CSS字体系列字符串)* 正文文本的字体系列。

* **footerTextColor***(CSS颜色字符串)* 辅助文本的颜色(如页脚文本和署名中的用户名)。

* **linkAttachmentBackgroundColor***(CSS颜色字符串)* 链接附件(堆叠附件)的背景颜色。

* **linkAttachmentBorderColor***(CSS颜色字符串)* 链接附件(堆叠附件)的边框颜色。

* **linkAttachmentColor***(CSS颜色字符串)* 链接附件文本的颜色。

* **链接颜色***(CSS颜色字符串)* 超链接的颜色(例如正文文本中的链接以及显示名称链接)。

* **TextColor***(CSS颜色字符串)* 正文文本的颜色。

* **titlefontSize***(CSS字体大小字符串)* 内容标题的字体大小。

* **titleLineHeight***(CSS行高度字符串)* 内容标题的行高。

* **SourceLogOcolor***(CSS颜色字符串)* 源标志的颜色。

* **userNameColor***(CSS颜色字符串)* 署名中用户名的颜色。
