---
description: 使用Javascript事件监听媒体墙中发生的事件，并将其发送到您选择的分析工具。
seo-description: 使用Javascript事件监听媒体墙中发生的事件，并将其发送到您选择的分析工具。
seo-title: 媒体墙的Javascript事件
solution: Experience Manager
title: 媒体墙的Javascript事件
uuid: afc0529-4640-476a-b207-91b2 c70101 f0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 媒体墙的Javascript事件{#javascript-events-for-media-wall}

使用Javascript事件监听媒体墙中发生的事件，并将其发送到您选择的分析工具。

Livefyre提供JavaScript事件，用于跟踪您的Livefyre应用程序中的用户活动。例如，当用户喜欢或共享内容至Twitter或Facebook或者发布新内容时，您可能希望更新页面。

以下是如何接收活动的示例。替换 `console.log` 为您的代码进行映射，并将事件发送到您的分析集成(动态标签管理、Adobe Analytics JS、Google Analytics等)：

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

支持的媒体墙事件的列表：

## 媒体墙事件

| Event | 定义 |
|---|---|
| `Init` | 当页面中包含媒体墙时。 |
| `Load` | 在不考虑位置的情况下，将媒体墙加载到页面上。 |
| `PostButtonClick` | 当用户单击媒体墙上的“上载按钮”时。 |
| `RequestMore` | 当用户在媒体墙中加载更多内容时。 |
| `TwitterReplyClick` | 当用户从“媒体墙”单击“Twitter回复”按钮时。 |
| `TwitterRetweetClick` | 当用户从媒体墙单击Twitter转推按钮时。 |
| `TwitterLikeClick` | 当用户从媒体墙单击“Twitter”/“收藏夹”按钮时。 |
| `ModalView` | 当用户单击以查看更大的模态窗口中的媒体墙内容时。 |
| `Like` | 当用户从媒体墙单击“赞”按钮时。 |
| `ShareButtonClick` | 每当用户单击“媒体墙”卡上的共享按钮时。 |
| `ShareURL` | 当“共享到URL”文本区域从媒体墙中进行选择/复制时。 |
| `ShareFacebook` | 当从“媒体墙”单击“共享到Facebook”时。 |
| `ShareTwitter` | 当从“媒体墙”单击“共享到Twitter”时。 |
