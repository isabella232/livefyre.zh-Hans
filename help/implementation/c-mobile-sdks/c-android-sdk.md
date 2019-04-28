---
description: 创建由Livefyre支持的Android应用程序。
seo-description: 创建由Livefyre支持的Android应用程序。
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793fa9-4890-b36 d-b631 f1 c6 f7 de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Android SDK{#android-sdk}

创建由Livefyre支持的Android应用程序。

使用此库将Livefyre服务集成到原生Android应用程序中。[Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) 根据Grale/Android Studio开发环境为我们的常见API机制提供了一个精简的图层。

Livefyre还提供 [了基于此SDK的评论](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) 示例应用程序。

此Livefyre Android SDK可用于Eclipse和Android Studio。

>[!NOTE]
>
>安装Livefyre Android SDK之前，您必须在环境中安装 [Android SDK](https://developer.android.com/sdk/index.html) 。如Android Developer docs&gt;中所述，您还必须包含一些其他Android SDK包。
>[添加SDK包](https://developer.android.com/sdk/installing/adding-packages.html)

使用Android SDK管理器(可从Android Studio或Eclipse工具栏中获取)安装所有推荐的包。一定要包含Android支持存储库。

## Eclipse {#section_dtm_slv_zz}

要在Eclipse中将Livefyre Android SDK添加到您的项目，请执行以下操作：

1. 从GitHub获得最新 [的StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) 。
1. 从现有项目开始或创建新项目。
1. 将StreamHub-Android-SDK导入工作区 **[!UICONTROL File > Import > General > Existing Project into Workspace]**中。
1. 浏览并选择StreamHub-Android-SDK；它现在应该在包资源管理器中显示。
1. 右键单击您的项目，然后选择 **[!UICONTROL Properties,]** Android选项卡。
1. 在“库”部分下，选择 **[!UICONTROL Add button,]** 库列表中的StreamHub-Android-SDK。
1. 单击 **[!UICONTROL Apply]****[!UICONTROL OK]**并单击。

## Android Studio {#section_vpw_klv_zz}

要在Android Studio中将Livefyre Android SDK添加到您的项目，请执行以下操作：

1. 从GitHub获得最新 [的StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) 。
1. 从现有项目开始或创建新项目。
1. 右键单击项目并选择 **[!UICONTROL Open Module Settings]**。
1. 选择窗口左上角的 **[!UICONTROL +]** 按钮。
1. 选择( **[!UICONTROL Import Existing Project.]** 在Android工作室的新版本中，您可以找到 **[!UICONTROL Import Existing Project]****[!UICONTROL More Modules]**。)

1. 浏览并选择StreamHub-Android-SDK。

Android Studio可能要求您将SDK转换为灰显版本；如果发生这种情况 **[!UICONTROL next]****[!UICONTROL finish]**，则选择。

在依赖关系下转至 **项目文件夹&gt; app文件夹&gt; build. grale** 文件以添加以下依赖关系：

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

确保以 **项目文件夹&gt; settings. grele** 文件的形式出现以下代码行：

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>您可以从Config. java自定义配置。

## 客户端 {#section_yfq_blv_zz}

StreamHub Android SDK显示若干可用于请求Livefyre API端点的客户端类：

* **SocialClient** 交换用户信息、密钥和其他元数据的用户身份验证令牌。

* **bootstrustClient** 获取有关特定集合的最近内容和元数据。

* **streamClient** 轮询集合的流以检索新的、更新的和已删除的内容。

* **WriteClient** 帖子、标记和类似集合中的内容。

