---
description: 将userPrivacyOptOut标记添加到页面，以允许站点访客退出此跟踪。
seo-description: 将userPrivacyOptOut标记添加到页面，以允许站点访客退出此跟踪。
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bbce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a

---


# userPrivacyOptOut{#userprivacyoptout}

向页面 `userPrivacyOptOut` 添加标志，以允许站点访客退出此跟踪。

Livefyre提供JavaScript事件以跟踪Livefyre应用程序中的用户活动。

如果您嵌入了Livefyre应用程序，而访客不同意跟踪，则可以动态配置Livefyre以禁用功能，以确保访客的隐私。

配置后，Livefyre将：

* 禁用应用程序中的身份验证支持。
* 禁用Livecount和事件生成
* 删除页面上任何应用程序创建的现有Cookie
* 代理媒体（带有来自第三方域的图像）以防止第三方创建Cookie
* 为需要额外单击才能查看的第三方视频启用视频蒙版点进

## 为退出配置页面

嵌入Livefyre应用程序的集成功能可在站点访问者未通过单个JavaScript变量授予许可的情况下配置Livefyre。

说明:

1. 将标 `userPrivacyOptOut` 志添加到 `Livefyre.js` JavaScript前的页面：

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. 添加 `Livefyre.js` 到页面之后的任意位置 `userPrivacyOptOut`。

   Livefyre应用程序使用提升的隐私设置进行实例化。

   >[!NOTE]
   >
   >加载Livefyre应用程序后， `userPrivacyOptOut` 请勿更改其值。

确保您的同意工作流程在 `userPrivacyOptOut` 网站访客选择退出时将设置为true。
