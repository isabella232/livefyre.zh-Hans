---
description: 用于在您的站点上为Livefyre提供支持的核心Livefyre库。
title: Livefyre.js
uuid: null
exl-id: 5f60ce54-5669-4768-912d-c1b13946d8b8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# updateAnchors方法{#updateAnchorsMethod}

使用updateAnchors方法将指示的内容动态添加到页面。

此方法对于分页或将可表示的内容动态添加到页面的其他情况很有用。 此方法为匹配的元素定义新锚点，并采用一个参数：newSelectors。

**newSelectors**。要添加到Siestr的选择器。 这可以是选择器字符串、jQuery对象或元素数组（应用程序构建期间传递的选择器参数接受的任何类型）。
格式:

```
app.updateAnchors(newSelectors);
```

示例：

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
