---
description: 您可以将视频域列入白名单。
seo-description: 您可以将视频域列入白名单。
seo-title: userPrivacyVideoHiteList
solution: Experience Manager
title: userPrivacyVideoHiteList
uuid: adfead18-b73 b-4ac4-97a0-d39 f528 b7606
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# userPrivacyVideoHiteList{#userprivacyvideowhitelist}

如果您使用自己的自定义视频和播放器作为Livefyre可视化应用程序中显示的视频的一部分，则可以将视频域列入白名单。将视频域列入白名单会删除自定义视频和播放器的视频遮罩。

>[!NOTE]
>
>使用特定路径确保只有安全的视频已列入白名单。如果您放置了一条宽阔的路径(例如sampledomain.com)，您可能会列入白名单。

* 添加 `userPrivacyVideoWhitelist``userPrivacyOptOut`之后。您可以一次性将所有Livefyre隐私标记添加到一个Livefyre对象中。
* `userPrivacyVideoWhitelist` 只适用于未从社交媒体嵌入的内容。

在以下示例中，在包含 `sampledomain.com/cdn/videos` 路径的应用程序中显示的视频已列入白名单：

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
