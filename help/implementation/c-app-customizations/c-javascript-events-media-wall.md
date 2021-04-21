---
description: 使用Javascript事件监听在媒体墙中发生的事件，并将它们发送到您选择的分析工具。
title: 适用于媒体墙的Javascript事件
exl-id: 3fe76467-65e2-4f8b-bd75-5a2ffc3e7e15
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# 媒体墙的Javascript事件{#javascript-events-for-media-wall}

使用Javascript事件监听在媒体墙中发生的事件，并将它们发送到您选择的分析工具。

Livefyre提供JavaScript事件，可跟踪Livefyre应用程序中的用户活动。 例如，您可能希望在用户喜欢或共享内容到Twitter或Facebook或发布新内容时更新页面。

以下是如何接收事件的示例。 将`console.log`替换为映射事件并将其发送到您的分析集成(动态标签管理、Adobe Analytics JS、Google Analytics等)的代码：

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

列表支持的媒体墙事件:

## 媒体墙事件

| 事件 | 定义 |
|---|---|
| `Init` | 当页面中包含媒体墙时。 |
| `Load` | 在页面上加载媒体墙时（无论位置如何）。 |
| `PostButtonClick` | 当用户单击媒体墙上的“上载”按钮时。 |
| `RequestMore` | 当用户在媒体墙中加载更多内容时。 |
| `TwitterReplyClick` | 当用户从媒体墙单击Twitter回复按钮时。 |
| `TwitterRetweetClick` | 当用户单击媒体墙中的Twitter转推按钮时。 |
| `TwitterLikeClick` | 当用户单击媒体墙中的“Twitter赞”/“收藏夹”按钮时。 |
| `ModalView` | 当用户在更大的模态窗口中单击到“视图媒体墙”内容时。 |
| `Like` | 当用户单击媒体墙中的“赞”按钮时。 |
| `ShareButtonClick` | 用户单击媒体墙卡上的共享按钮时。 |
| `ShareURL` | 当从“媒体墙”中选择/复制“共享到URL”文本区域时。 |
| `ShareFacebook` | 从“媒体墙”单击“共享到Facebook”时。 |
| `ShareTwitter` | 从“媒体墙”单击“共享到Twitter”时。 |
