---
description: 创建媒体墙，实时实现内容流。
seo-description: 创建媒体墙，实时实现内容流。
seo-title: 媒体墙
solution: Experience Manager
title: 媒体墙
uuid: c6087c80-a35b-44d2-9dd4-ba9cd47172d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 媒体墙{#media-wall}

创建媒体墙，实时实现内容流。

通过媒体墙，您可以为网站创建实时社交墙。 使用Livefyre javaScript SDK的streamhub-wallpackage将Livefyre社交源显示为一种视觉上引人入胜的、全屏拼贴的内容体验，它非常适合用于覆盖实时活动、主持照片竞赛以及为您的网站的社交部分提供强大动力。

## 集成 {#section_jfm_bwb_c1b}

添加媒体墙的最快捷方式是使用Livefyre的CDN上托管的构建版本。

首先，将 [Livefyre.js添加到您的站点](https://github.com/Livefyre/Livefyre.js) 。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

然后，将显示“媒体墙”的元素放置到其中。

```
<div id="wall"></div>
```

最后，使用 `Livefyre.require` 来构建组件。

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

你现在有墙了！ 请在此示例中查看所有 [操作情况](https://codepen.io/gobengo/pen/dFwDL)。

**是否点击错误？** 检查以确保传递的环境参数正确。 选项包 `livefyre.com` 括（生产） `t402.livefyre.com` 或(UAT)。

>[!NOTE]
>
>您的媒体墙应用程序呈现的帖子的任何样式自定义都必须根据Twitter的“显示要求” [进行](https://dev.twitter.com/terms/display-requirements)。

## 配置选项 {#section_ucv_qvb_c1b}

`columns`

允许您在构建媒体墙时定义媒体墙的列数。 如果设置此选项，则每列的宽度将自动适应媒体墙的容器大小，同时保持指定的列数。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

载入页面时要呈现的内容项数。 默认为50。

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

允许您为“媒体墙”的容器元素内的每列设置最小（像素）宽度。 (您的媒体墙将根据其容器元素的宽度自动选择适当的列数。 默认情况下，媒体墙的宽度除以最小内容宽度（如果未定义，则为300px）将决定列数。)

>[!NOTE]
>
>请勿将此选项与列选项结合使用。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

默认情况下，当内容有附件时，媒体墙将显示可单击的缩略图。 单击后，应用程序将打开一个模态，显示整个照片／视频附件。 要禁用此选项，请将modal设置为false。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

定义要 [!UICONTROL Post Content] 显示在墙上的按钮。 此选项要求您传入， `opts.collection`并向页面添加Livefyre.js身份验证集成。

`postButton` 参数：

* `false` （默认）:不显示“发布内容”按钮。 （创建只读媒体墙。）
* `true` (或 `LiveMediaWall.postButtons.contentWithPhotos`):包含一个按钮，允许用户添加包含附加照片的文本内容。

* `LiveMediaWall.postButtons.content`:包括允许用户添加文本内容但不附加照片的按钮。
* `LiveMediaWall.postButtons.photo`:包括允许用户添加照片但不添加文本的按钮。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

定义在单击按钮时要添加到墙中的内 [!UICONTROL Show More] 容项目数。

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## 样式配置选项 {#section_ztv_dvb_c1b}

Media Wall还提供多个配置选项，允许您自定义文本颜色、样式和大小。 要实现这些选项，请使用以下语法：

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

有关有效输入，请参阅CSS字体系列、字体大小 [、行高](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family)、Color属性的W3C [标准](https://www.w3.org/TR/CSS2/fonts.html#font-size-props)[](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height)[](https://www.w3.org/TR/css3-color/#colorunits) 。

* **bodyFontSize** (CSS字体大小 *字符串)* 内容正文文本的字体大小。

* **bodyLineHeight** （CSS行高字符串） ** ，内容正文文本的行高。

* **buttonActiveBackgroundColor** (CSS Color String) ***活动时按钮背景的颜色。

* **buttonBorderColor** (CSS颜色 *字符串)**按钮边框的颜色。

* **buttonHoverBackgroundColor** （CSS颜色字符串） ** 悬停时按钮背景的颜色。

* **buttonTextColor** (CSS颜色 *字符串)* 按钮标签的颜色。

* **cardBackgroundColor** (CSS Color String) ** Media wall中内容卡的背景颜色。

* **displayNameColor** (CSS Color String) ** by行中显示名称的颜色。

* **fontFamily** (CSS字 *体系列字符串)* 正文文本的字体系列。

* **footerTextColor** (CSS Color String) ** 辅助文本的颜色（如页脚文本和署名中的用户名）。

* **linkAttachmentBackgroundColor** (CSS Color String) ** 链接附件（堆叠附件）的背景颜色。

* **linkAttachmentBorderColor** (CSS Color String) ** 链接附件（堆叠附件）的边框颜色。

* **linkAttachmentTextColor** (CSS颜色 *字符串)* 链接附件文本的颜色。

* **linkColor** (CSS Color String) ** 超链接的颜色（如正文文本中的链接和显示名称链接）。

* **textColor** (CSS颜 *色字符串)* 正文文本的颜色。

* **titleFontSize** (CSS字 *体大小字符串)* 内容标题的字体大小。

* **titleLineHeight** (CSS行高字 *符串)* ，内容标题的行高。

* **sourceLogoColor** (CSS颜 *色字符串)* 源徽标的颜色。

* **usernameColor** (CSS Color String) ** Byline中用户名的颜色。
