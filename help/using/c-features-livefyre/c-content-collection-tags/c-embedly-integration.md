---
description: 使用 embed.ly 直接在应用程序中显示多种媒体格式。
seo-description: 使用 embed.ly 直接在应用程序中显示多种媒体格式。
seo-title: Embedly 集成
solution: Experience Manager
title: Embedly 集成
uuid: 1f27e32c-c2c3-4f7c-93de-c9c7bf783d6a
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 14%

---


# Embedly 集成{#embedly-integration}

使用`embed.ly`直接在应用程序中显示多种媒体格式。

为了更好地支持来自各种来源（包括Google Maps、YouTube、Flickr、Facebook、Instagram、Spotify和Tumblr）的嵌入式媒体内容，Livefyre Apps将Embedly用作URL扩展的第三方提供商。 如果用户或审查方在帖子中包含受支持的链接，则在将链接中包含的媒体发布到集合时，该媒体将会扩展。

这使Livefyre应用程序能够访问Embedly支持的250多种不同的嵌入式媒体选项。

>[!NOTE]
>
>Livefyre仅扩展Embedly的完整提供商列表的子集。 仅当提供者是Twitter、YouTube、Imgur、Vine、Wikipedia或SoundCloud时，嵌入的图像才会在HTTPS页面上扩展。 有关链接扩展或源的任何其他问题，请与您的技术客户经理联系。

本页列表了一些常用嵌入式媒体类型及其可接受的URL模式的示例。 `Embed.ly` 不断增加新来源。有关提供程序的完整列表，请访问`https://embed.ly/embed/features/providers`。

>[!NOTE]
>
>嵌入式格式要求完全权限。 缩短的链接不起作用。

只有可嵌入的公开内容。 如果您尝试嵌入非公开的内容，则指向该内容的链接将显示在博客文章中，并且该内容旁边将显示一个占位符图标。 单击该链接后，读者将从托管内容的服务收到错误消息，如仅好友照片的Facebook消息。 如果您注意到媒体未按预期方式展开，请与客户经理联系。

## 示例嵌入式URL

| 类型 | 提供商 | URL |
|--- |--- |--- |
| 地图 | Google地图 | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**注意**:URL必须以开 `http` 头，而非  `https.` |
| 社交网络 | Google+ | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| 视频 | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| 照片 | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | TwitPic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` （Hootsuite的内容上传服务） | `https://ow.ly/i/*` |
| 投票 | GoPollGo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Droplr | `https://d.pr/i/*` |
| 音频 | SoundCloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| 博客 | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

使用此功能的应用程序：

* [轮播](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [评论](/help/using/c-about-apps/c-comments/c-comments.md)
* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地图](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [媒体墙](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [马赛克](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [投票](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [评论](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidesk](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [趋势](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [上传按钮](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

