---
description: 使用 embed.ly 直接在应用程序中显示多种媒体格式。
seo-description: 使用 embed.ly 直接在应用程序中显示多种媒体格式。
seo-title: Embedly 集成
solution: Experience Manager
title: Embedly 集成
uuid: 1f27e32c-c2 c3-4f7 c-93de-c9 c7 f783 d6 a
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Embedly 集成{#embedly-integration}

用于 `embed.ly` 直接在应用程序中显示多种媒体格式。

为了更好地支持来自各种来源的嵌入式媒体内容，包括Google地图、YouTube、Flickr、Facebook、Instagram、Spack和Tumblr，Livefyre应用程序将Embey作为URL扩展的第三方提供商使用。如果用户或主持人在帖子中包含受支持的链接，则在发布到集合时，链接中包含的媒体将展开。

这为Livefyre应用程序提供了对250种不同的嵌入媒体选项(Embyy支持)的访问权限。

>[!NOTE]
>
>Livefyre仅扩展Embeyly完整提供商列表的子集。仅当提供商为Twitter、YouTube、IMGur、藤蔓、维基百科或SoundCloud时，嵌入式图像才会在HTTPS页面上展开。有关链接扩展或源的任何其他问题，请与技术客户经理联系。

本页列出了一些常用的嵌入式媒体类型及其可接受的URL模式示例。`Embed.ly` 不断增加新来源。有关提供商的完整列表 `https://embed.ly/embed/features/providers`，请访问。

>[!NOTE]
>
>基本格式需要完全的权限。缩短的链接将不起作用。

只有可供查看的内容才可嵌入。如果尝试嵌入不公开的内容，则该内容的链接将显示在博客文章中，并且占位图标将伴随它。单击该链接后，链接会将读者带到托管内容的服务中的错误消息，如仅适用于朋友的照片的Facebook消息。如果您注意到媒体未按预期展开，请联系您的客户经理。

## 示例嵌入URL

| Type | 提供商 | URL |
|--- |--- |--- |
| 地图 | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**注意**：URL必须以 `http` 而非 `https.` |
| 社交网络 | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| 视频 | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| 照片 | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | Twitch | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Hootsuite的内容上传服务) | `https://ow.ly/i/*` |
| 投票 | GoPowergo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Dropr | `https://d.pr/i/*` |
| 音频 | SoundCloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spetify | `https://open.spotify.com/*` |
| 博客 | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

使用此功能的应用程序：

* [Carousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [注释](/help/using/c-about-apps/c-comments/c-comments.md)
* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地图](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [媒体墙](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaic](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [投票](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [评论](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Siten表示](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [趋势趋势](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [上传按钮](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

