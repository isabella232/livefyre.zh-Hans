---
description: 用于在您的站点上为Livefyre提供支持的核心Livefyre库。
seo-description: 用于在您的站点上为Livefyre提供支持的核心Livefyre库。
seo-title: updateAnchors方法
solution: Experience Manager
title: Livefyre.js
uuid: null
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 1%

---


# updateAnchors方法{#updateAnchorsMethod}

使用updateAnchors方法将指示的内容动态添加到页面。

此方法对于分页或在可动态将字号内容添加到页面的其他情况下非常有用。 此方法为匹配的元素定义新锚点，并采用单个参数：newSelectors。

**newSelectors**。要添加到Sidestr的选择器。 这可以是选择器字符串、jQuery对象或元素数组（在应用程序构建过程中传递的选择器参数接受的任何类型）。
格式:

```
app.updateAnchors(newSelectors);
```

示例：

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
