---
description: 使用Javascript事件监听在媒体墙中发生的事件，并将其发送到您选择的分析工具。
seo-description: 使用Javascript事件监听在媒体墙中发生的事件，并将其发送到您选择的分析工具。
seo-title: 媒体墙的Javascript事件
solution: Experience Manager
title: 媒体墙的Javascript事件
uuid: 8afc0529-4640-476a-b207-91b2c70101f0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 媒体墙的Javascript事件{#javascript-events-for-media-wall}

使用Javascript事件监听在媒体墙中发生的事件，并将其发送到您选择的分析工具。

Livefyre提供JavaScript事件以跟踪Livefyre应用程序中的用户活动。 例如，当用户喜欢或共享内容到Twitter或Facebook，或者发布新内容时，您可能希望更新页面。

以下是如何接收事件的示例。 替换 `console.log` 您的代码，将事件映射并发送到您的分析集成（动态标签管理、Adobe Analytics JS、Google Analytics等）:

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

支持的媒体墙事件列表：

## 媒体墙事件

| 事件 | 定义 |
|---|---|
| `Init` | 当媒体墙包含在页面中时。 |
| `Load` | 将媒体墙加载到页面上时，无论位置如何。 |
| `PostButtonClick` | 当用户单击媒体墙上的上传按钮时。 |
| `RequestMore` | 当用户在媒体墙中加载更多内容时。 |
| `TwitterReplyClick` | 当用户单击“媒体墙”中的“Twitter回复”按钮时。 |
| `TwitterRetweetClick` | 当用户单击媒体墙中的“Twitter转推”按钮时。 |
| `TwitterLikeClick` | 当用户单击“媒体墙”中的“Twitter赞／喜爱”按钮时。 |
| `ModalView` | 当用户单击以在更大的模态窗口中查看媒体墙内容时。 |
| `Like` | 当用户单击媒体墙中的“赞”按钮时。 |
| `ShareButtonClick` | 用户单击媒体墙卡上的共享按钮时。 |
| `ShareURL` | 当从“媒体墙”中选择／复制“共享到URL”文本区域时。 |
| `ShareFacebook` | 当从媒体墙单击“共享到Facebook”时。 |
| `ShareTwitter` | 从媒体墙单击“共享到Twitter”时。 |
