---
description: 您可以使用将视频域列入白名单。
seo-description: 您可以使用将视频域列入白名单。
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

如果您将您自己的自定义视频和播放器用作Livefyre可视化应用程序中显示的视频的一部分，则可以将您的视频域列入白名单。 将视频域列入白名单可删除自定义视频和播放器的视频蒙版。

>[!NOTE]
>
>使用特定路径确保仅将安全的视频列入白名单。 如果您选择了一条宽广的路径（例如，sampledomain.com），则可能会将不安全视频列入白名单。

* 添加 `userPrivacyVideoWhitelist` 后 `userPrivacyOptOut`面。 您可以同时添加所有Livefyre隐私权标志，作为一个Livefyre对象的一部分。
* `userPrivacyVideoWhitelist` 仅适用于未从社交媒体嵌入的内容。

在以下示例中，在具有路径的应用程序中显示的视 `sampledomain.com/cdn/videos` 频列入白名单：

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
