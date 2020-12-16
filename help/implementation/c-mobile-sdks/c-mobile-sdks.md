---
description: 将Livefyre添加到您的本机移动应用程序。
seo-description: 将Livefyre添加到您的本机移动应用程序。
seo-title: Mobile SDK
solution: Experience Manager
title: Mobile SDK
uuid: 84c7ca1c-3401-492a-bfa5-62b996947a44
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 5%

---


# Mobile SDK{#mobile-sdks}

将Livefyre添加到您的本机移动应用程序。

根据您计划进行的自定义程度，移动实施有多种可用选项：

* 移动Web应用程序
* Livefyre Android或iOS SDK
* HTTP API

## 移动Web应用程序{#section_t2k_vpb_11b}

在移动设备上打开网页的客户可自动获得针对移动设备进行了优化的Livefyre内容流，包括适合缩小屏幕大小的样式和处理触摸事件的修改。

>[!NOTE]
>
>在Android WebView中使用Livefyre应用程序时，Android [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html)参数必须设置为true。 如果未启用localStorage，则Livefyre将无法将用户登录到Livefyre应用程序。

为了针对移动设备进行优化，Livefyre将“注释”、“实时博客”和“聊天应用程序”功能集限制为：

* 帖子
* 编辑
* 标记
* 点赞
* 回复
* 监听器计数
* 注释计数
* 内联挂起审核
* 气垫船
* 热门评论
* 热线程
* 队列注释

在移动Web应用程序中，单击作者姓名将在新页面中打开悬浮卡信息。

## Livefyre Android SDK或iOS SDK {#section_zdz_spb_11b}

Livefyre还提供两个移动SDK:iOS SDK和Android SDK。 这些SDK是我们HTTP端点周围的包裹，旨在提供更轻松的数据发送和接收方法。 这些SDK不提供界面，因此在内容的显示和使用方式方面具有更大的灵活性。

Android和iOS SDK支持评论、实时博客和聊天的以下功能：

| iOS功能： | Android功能： |
|--- |--- |
| <ul><li> 帖子 </li><li>编辑 </li><li>标记 </li><li>点赞 </li><li>回复 </li><li>热线程</li></ul> | <ul><li>帖子 </li><li>编辑 </li><li>点赞 </li><li>回复 </li><li>热线程</li></ul> |

## HTTP API {#section_yqb_qpb_11b}

HTTP API是端点组，它允许您在Livefyre平台上创建对话和内容。 它还为所有开箱即用的Livefyre流提供动力。 虽然此解决方案需要您的工程团队投入更多的开发时间，但它在使用Livefyre产品套件时提供了更大的灵活性，并允许本机移动集成。

>[!IMPORTANT]
>
>**不要** 在移动客户端中创建用户身份验证令牌，因为这要求您在不安全的应用程序中公开Livefyre密钥。要获得更可靠、更安全的解决方案，请参阅用户身份验证令牌部分。

