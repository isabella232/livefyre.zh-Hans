---
description: 将userPrivacyOptOut标志添加到页面，以允许站点访客选择退出此跟踪。
seo-description: 将userPrivacyOptOut标志添加到页面，以允许站点访客选择退出此跟踪。
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bbce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# userPrivacyOptOut{#userprivacyoptout}

将`userPrivacyOptOut`标志添加到页面，以允许站点访客选择退出此跟踪。

Livefyre提供JavaScript事件来跟踪Livefyre应用程序中的用户活动。

如果您嵌入Livefyre应用程序，而访客不同意跟踪，则可以动态配置Livefyre以禁用功能，以确保访客的隐私。

配置后，Livefyre将：

* 禁用应用程序中的身份验证支持。
* 禁用Live Count和事件生成
* 删除页面上任何应用程序创建的现有Cookie
* 代理媒体与来自第三方域的图像，以防止第三方创建Cookie
* 为需要额外单击才能视图的第三方视频启用视频蒙版点进

## 配置退出页面

嵌入Livefyre应用程序的集成在站点访客未通过单个JavaScript变量授予同意时，可以配置Livefyre。

说明:

1. 将`userPrivacyOptOut`标志添加到`Livefyre.js` JavaScript之前的页面：

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. 将`Livefyre.js`添加到`userPrivacyOptOut`后的任意位置。

   使用提升的隐私设置实例化Livefyre应用程序。

   >[!NOTE]
   >
   >加载Livefyre应用程序后，请勿更改`userPrivacyOptOut`的值。

如果站点访客选择这样做，请确保您的同意工作流将`userPrivacyOptOut`设置为选择退出true。
