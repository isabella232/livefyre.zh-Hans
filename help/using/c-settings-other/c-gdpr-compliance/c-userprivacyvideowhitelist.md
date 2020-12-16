---
description: 您可以允许列出您的视频域。
seo-description: 您可以允许列出您的视频域。
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

如果您将您自己的自定义视频和播放器用作Livefyre可视化应用程序中显示的视频的一部分，则可以允许列出您的视频域。 允许列出您的视频域将删除自定义视频和播放器的视频蒙版。

>[!NOTE]
>
>使用特定路径确保仅允许列出安全的视频。 如果您放宽了路径（例如，sampledomain.com），则可能允许列出不安全视频。

* 在`userPrivacyOptOut`后添加`userPrivacyVideoWhitelist`。 您可以一次添加所有Livefyre隐私标志，作为一个Livefyre对象的一部分。
* `userPrivacyVideoWhitelist` 仅适用于未从社交媒体嵌入的内容。

在以下示例中，允许列出在具有`sampledomain.com/cdn/videos`路径的应用程序中显示的视频：

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
