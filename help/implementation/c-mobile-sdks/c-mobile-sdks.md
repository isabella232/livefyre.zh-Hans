---
description: 将Livefyre添加到您的本机移动应用程序。
seo-description: 将Livefyre添加到您的本机移动应用程序。
seo-title: 移动SDK
solution: Experience Manager
title: 移动SDK
uuid: 84c7ca1c-341-492a-bfa5-62b996947 a44
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 移动SDK{#mobile-sdks}

将Livefyre添加到您的本机移动应用程序。

有若干可用于移动实施的选项，具体取决于您计划进行的自定义设置：

* 移动Web应用程序
* Livefyre Android或iOS SDK
* HTTP API

## 移动Web应用程序 {#section_t2k_vpb_11b}

在移动设备上打开网页的客户会自动获得一个针对移动设备优化的Livefyre内容流，包括样式以适合更小的屏幕大小和修改，以处理触摸事件。

>[!NOTE]
>
>在Android WebView中使用Livefyre应用程序时，Android [WebSettings. setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) 参数必须设置为true。如果未启用LocalStorage，Livefyre将无法将用户登录到Livefyre应用程序。

为了优化移动设备，Livefyre将评论、Live Blog和聊天应用程序功能集限制为包括：

* Post
* 编辑
* 旗标
* 赞一样
* Reply
* 监听器计数
* 评论计数
* 内联待定审核
* 超卡
* 热门评论
* 热门线程
* 队列注释

在Mobile Web应用程序中，单击作者姓名可打开新页面中的自动卡信息。

## Livefyre Android SDK或iOS SDK {#section_zdz_spb_11b}

Livefyre还提供了两个移动SDK：iOS SDK和Android SDK。这些SDK围绕我们的HTTP端点进行打包，它们为提供和接收数据提供了一种更简单的方法。这些SDK没有提供接口，使您能够更灵活地在移动应用程序中显示和使用内容。

Android和iOS SDK支持评论、Live Blog和聊天的以下功能：

| iOS功能： | Android功能： |
|--- |--- |
| <ul><li> Post </li><li>编辑 </li><li>旗标 </li><li>赞一样 </li><li>Reply </li><li>热门线程</li></ul> | <ul><li>Post </li><li>编辑 </li><li>赞一样 </li><li>Reply </li><li>热门线程</li></ul> |

## HTTP API {#section_yqb_qpb_11b}

HTTP API是一组端点，允许您在Livefyre平台上创建对话和内容。它还使所有Livefyre摆脱了框流。虽然此解决方案需要从您的工程团队获得更多的开发时间，但它在使用Livefyre产品套件时提供了更高的灵活性，并允许本机移动集成。

>[!IMPORTANT]
>
>**请勿** 在移动客户端中创建用户身份验证令牌，因为这会要求您在不安全的应用程序中暴露Livefyre机密网络密钥。有关更可靠和安全的解决方案，请参阅“用户身份验证令牌”部分。

