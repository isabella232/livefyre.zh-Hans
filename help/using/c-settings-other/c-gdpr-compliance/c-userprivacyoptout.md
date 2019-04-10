---
description: 将userPrivacyoptOut标记添加到页面，以允许站点访问者退出此跟踪。
seo-description: 将userPrivacyoptOut标记添加到页面，以允许站点访问者退出此跟踪。
seo-title: userPrivacyOptout
title: userPrivacyOptout
uuid: a043c50e -a02-4c83-bbce-54b9 b51316 a5
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# userPrivacyOptout{#userprivacyoptout}

将 `userPrivacyOptOut` 标记添加到页面，以允许站点访问者退出此跟踪。

Livefyre提供JavaScript事件，用于跟踪您的Livefyre应用程序中的用户活动。

如果您嵌入Livefyre应用程序且访客不同意跟踪，则可以动态配置Livefyre以禁用功能以确保访客的隐私。

配置后，Livefyre将：

* 禁用应用程序中的身份验证支持。
* 禁用Live Copy和事件生成
* 删除页面上任何应用程序创建的现有Cookie
* 使用第三方域中的图像的代理媒体，以防止第三方创建cookie
* 为第三方视频启用视频蒙版点击，该选项需要另外单击一下以查看

## 配置页面以退出

集成嵌入Livefyre应用程序可在站点访问者使用单个JavaScript变量未授予同意时配置Livefyre。

说明：

1. 在JavaScript之前，将 `userPrivacyOptOut` 标记添加 `Livefyre.js` 到页面中：

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. 在任何位置添加 `Livefyre.js` 到页面 `userPrivacyOptOut`。

   Livefyre应用程序利用提升的隐私设置进行实例化。

   >[!NOTE]
   >
   >请勿更改Livefyre应用程序加载 `userPrivacyOptOut` 后的价值。

如果站点访问者选择退出，确保您的同意工作流将其 `userPrivacyOptOut` 设置为true。
