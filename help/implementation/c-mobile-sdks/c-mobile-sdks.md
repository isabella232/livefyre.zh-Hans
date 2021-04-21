---
description: 将Livefyre添加到您的本机移动应用程序。
title: Mobile SDK
exl-id: e05001a4-6199-4d98-a661-123e031b657b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 4%

---

# Mobile SDK{#mobile-sdks}

将Livefyre添加到您的本机移动应用程序。

根据您计划进行的自定义范围，移动实施有多种可用选项：

* 移动Web应用程序
* Livefyre Android或iOS SDK
* HTTP API

## 移动Web应用程序{#section_t2k_vpb_11b}

在移动设备上打开网页的客户会自动获得针对移动设备进行了优化的Livefyre内容流，包括根据缩小的屏幕尺寸设计样式以及为处理触摸事件而做的修改。

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
* 气垫运动卡
* 热门评论
* 热线程
* 队列注释

在移动Web应用程序中，单击作者姓名将在新页面中打开悬浮卡信息。

## Livefyre Android SDK或iOS SDK {#section_zdz_spb_11b}

Livefyre还提供两个移动SDK:iOS SDK和Android SDK。 这些SDK是我们的HTTP端点周围的包装，旨在提供更轻松的数据发送和接收方法。 这些SDK不提供任何界面，因此在内容在您的移动应用程序中的显示和使用方面具有更大的灵活性。

Android和iOS SDK支持评论、实时博客和聊天的以下功能：

| iOS功能： | Android功能： |
|--- |--- |
| <ul><li> 帖子 </li><li>编辑 </li><li>标记 </li><li>点赞 </li><li>回复 </li><li>热线程</li></ul> | <ul><li>帖子 </li><li>编辑 </li><li>点赞 </li><li>回复 </li><li>热线程</li></ul> |

## HTTP API {#section_yqb_qpb_11b}

HTTP API是端点组，允许您在Livefyre平台上创建对话和内容。 它还为所有Livefyre提供开箱即用的流。 虽然此解决方案需要您的工程团队投入更多开发时间，但在使用Livefyre产品套件时却提供了更大的灵活性，并允许本机移动集成。

>[!IMPORTANT]
>
>**请勿** 在移动客户端中创建用户身份验证令牌，因为这要求您在不安全的应用程序中公开您的Livefyre密钥。有关更强大和安全的解决方案，请参阅用户身份验证令牌部分。
