---
description: 定义用户可以发布媒体的来源，以及禁止发布媒体的来源。
seo-description: 定义用户可以发布媒体的来源，以及禁止发布媒体的来源。
seo-title: 管理嵌入式媒体
title: 管理嵌入式媒体
uuid: d8621be1-dcfb-429f-954e-b21fdcf02715
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 管理嵌入式媒体{#manage-embedded-media}

定义用户可以发布媒体的来源，以及禁止发布媒体的来源。

默认情况下，所有媒体附件都可以嵌入到注释中。 有关受支持提供商的完整列表，请参阅embed.ly/providers。

Livefyre使用Embed.ly和标准的oEmbed协议将媒体嵌入到应用程序流中，并将通过其源提供的所有媒体数据。

Embed.ly将传递所有可用信息，包括媒体的标题、描述、缩略图和任何提供的URL的嵌入代码。 这些项目的可用性因提供商而异。 例如：Facebook不会返回其视频的缩略图，并且只传递可嵌入的视频。 单击“播放”将启动视频（与YouTube的显示格式类似）。 Twitter仅传递静态图像，不发送视频。 因此，Twitter本机视频可能不会从Livefyre流中播放。

嵌入注释流时，您可能会阻止某些附件嵌入到注释中。 您还可以选择使用Studio隐藏网络、站点和对话级别上的所有Embed.ly扩展，仅显示指向媒体的链接，而不显示完全嵌入的媒体。

使用此功能的应用程序：

* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地图](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [媒体墙](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)

