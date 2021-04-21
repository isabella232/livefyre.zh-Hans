---
description: 创建由Livefyre提供支持的Android应用程序。
title: Android SDK
exl-id: 54ea6537-5f27-4174-af25-d17257f23e48
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 1%

---

# Android SDK{#android-sdk}

创建由Livefyre提供支持的Android应用程序。

使用此库将Livefyre服务集成到您的本机Android应用程序中。 [Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK)根据Gradle/Android Studio开发环境，围绕我们的常见API机制提供了一个精简层。

Livefyre还基于此SDK提供[Reviews](https://github.com/Livefyre/StreamHub-iOS-Reviews-App)示例应用程序。

此Livefyre Android SDK可用于Eclipse和Android Studio。

>[!NOTE]
>
>在安装Livefyre Android SDK之前，您的环境上必须安装[Android SDK](https://developer.android.com/sdk/index.html)。 您还必须包括某些其他Android SDK包，如Android开发人员文档>中所述。
>[添加SDK包](https://developer.android.com/sdk/installing/adding-packages.html)

使用Android SDK Manager（可从Android Studio或Eclipse工具栏获得）安装所有建议的包。 请务必还包括Android支持存储库。

## Eclipse {#section_dtm_slv_zz}

要将Livefyre Android SDK添加到Eclipse中的项目，请执行以下操作：

1. 从GitHub获取最新的[StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK)。
1. 开始现有项目或创建新项目。
1. 要将StreamHub-Android-SDK导入工作区，请转至&#x200B;**[!UICONTROL File > Import > General > Existing Project into Workspace]**。
1. 浏览并选择StreamHub-Android-SDK;它现在应显示在包资源管理器中。
1. 右键单击您的项目，然后选择&#x200B;**[!UICONTROL Properties,]**，然后选择Android选项卡。
1. 在“库”部分下，选择&#x200B;**[!UICONTROL Add button,]**，然后从库的列表中选择StreamHub-Android-SDK。
1. 单击&#x200B;**[!UICONTROL Apply]**&#x200B;和&#x200B;**[!UICONTROL OK]**。

## Android Studio {#section_vpw_klv_zz}

要在Android Studio中将Livefyre Android SDK添加到您的项目，请执行以下操作：

1. 从GitHub获取最新的[StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK)。
1. 开始现有项目或创建新项目。
1. 右键单击项目并选择&#x200B;**[!UICONTROL Open Module Settings]**。
1. 选择窗口左上角的&#x200B;**[!UICONTROL +]**&#x200B;按钮。
1. 选择&#x200B;**[!UICONTROL Import Existing Project.]**（在新版Android studio中，您可以在&#x200B;**[!UICONTROL More Modules]**&#x200B;下找到&#x200B;**[!UICONTROL Import Existing Project]**。）

1. 浏览并选择StreamHub-Android-SDK。

Android Studio可能会要求您将SDK转换为Gradle版本；如果发生这种情况，请选择&#x200B;**[!UICONTROL next]**，然后选择&#x200B;**[!UICONTROL finish]**。

转到依赖项下的&#x200B;**项目文件夹> app folder > build.gradle**&#x200B;文件，添加以下依赖项：

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

确保以下代码行位于&#x200B;**项目文件夹> settings.gradle**&#x200B;文件中：

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>您可以从Config.java中自定义配置。

## 客户 {#section_yfq_blv_zz}

StreamHub Android SDK公开了几个可用于请求Livefyre API端点的客户端类：

* **AdminClient** 交换用户信息、密钥和其他元数据的用户身份验证令牌。

* **BootstrapClient** 获取有关特定集合的最新内容和元数据。

* **StreamClient** 轮询集合的流，以检索新的、更新的和删除的内容。

* **WriteClientPost** 、标记和类似集合中的内容。
