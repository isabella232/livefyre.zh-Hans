---
description: 将userPrivacyOptOut标志添加到页面，以允许站点访客此选择退出跟踪。
title: userPrivacyOptOut
exl-id: 1e935e69-60af-4151-905c-93a1cccbeb49
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# userPrivacyOptOut{#userprivacyoptout}

将`userPrivacyOptOut`标志添加到页面，以允许对此跟踪进行站选择退出点访客。

Livefyre提供JavaScript事件，可跟踪Livefyre应用程序中的用户活动。

如果您嵌入了Livefyre应用程序，而访客不同意跟踪，您可以动态配置Livefyre以禁用功能，以确保访客的隐私。

配置后，Livefyre将：

* 禁用应用程序中的身份验证支持。
* 禁用Livecount和事件生成
* 删除页面上任何应用程序创建的现有Cookie
* 使用来自第三方域的图像代理媒体，防止第三方创建Cookie
* 为需要额外单击才能视图的第三方视频启用视频蒙版点进

## 配置退出页面

嵌入Livefyre应用程序的集成功能可以在站点访客未通过单个JavaScript变量授予同意时配置Livefyre。

说明:

1. 将`userPrivacyOptOut`标志添加到`Livefyre.js` JavaScript之前的页面：

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. 将`Livefyre.js`添加到`userPrivacyOptOut`之后的任意位置。

   使用提升的隐私设置实例化Livefyre应用程序。

   >[!NOTE]
   >
   >加载Livefyre应用程序后，请勿更改`userPrivacyOptOut`的值。

确保您的同意工作流在站点访客选择时将`userPrivacyOptOut`设置为true选择退出。
