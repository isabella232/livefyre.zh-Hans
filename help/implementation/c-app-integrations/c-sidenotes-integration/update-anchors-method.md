---
description: 用于为站点上Livefyre供电的核心Livefyre库。
seo-description: 用于为站点上Livefyre供电的核心Livefyre库。
seo-title: UpdateAnchors方法
solution: Experience Manager
title: Livefyre. js
uuid: null
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# UpdateAnchors方法 {#updateAnchorsMethod}

使用updateAnchors方法将sited内容添加到页面中。

此方法可用于分页，或在动态将sixx可搜索内容添加到页面的其他情况下。此方法为匹配元素定义新锚点，并采用单个参数：NewsSelectors。

**NewsSelectors**。要添加到SiteNote的选择器。这可能是选择器字符串、jQuery对象或元素数组(在应用程序构造过程中通过的选择器参数所接受的任何类型)。
格式：

```
app.updateAnchors(newSelectors);
```

示例：

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
