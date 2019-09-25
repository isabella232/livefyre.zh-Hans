---
description: 创建由Livefyre提供支持的Android应用程序。
seo-description: 创建由Livefyre提供支持的Android应用程序。
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Android SDK{#android-sdk}

创建由Livefyre提供支持的Android应用程序。

使用此库将Livefyre服务集成到您的本机Android应用程序中。 Livefyre [StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) 基于Gradle/Android studio开发环境，围绕我们的常见API机制提供了一个精简层。

Livefyre还基于此SDK提 [供Reviews](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) 范例应用程序。

此Livefyre Android SDK可用于Eclipse和Android Studio。

>[!NOTE]
>
>在安装Livefyre Android SDK之前，您的环境中必须安 [装Android SDK](https://developer.android.com/sdk/index.html) 。 您还必须包括一些其他Android SDK包，如Android开发人员文档&gt;中所述。
>[添加SDK包](https://developer.android.com/sdk/installing/adding-packages.html)

使用Android SDK Manager（可从Android studio或Eclipse工具栏获得）安装所有建议的包。 请务必还包括Android支持存储库。

## Eclipse {#section_dtm_slv_zz}

要将Livefyre Android SDK添加到Eclipse中的项目，请执行以下操作：

1. 从GitHub获取最 [新的StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) 。
1. 从现有项目开始或创建新项目。
1. 要将StreamHub-Android-SDK导入工作区，请转至 **[!UICONTROL File > Import > General > Existing Project into Workspace]**。
1. 浏览并选择StreamHub-Android-SDK;它现在应显示在包资源管理器中。
1. 右键单击您的项目，然后选择 **[!UICONTROL Properties,]** Android选项卡。
1. 在“库”部分下，选 **[!UICONTROL Add button,]** 择，然后从库列表中选择StreamHub-Android-SDK。
1. 单击和 **[!UICONTROL Apply]** “” **[!UICONTROL OK]**。

## Android Studio {#section_vpw_klv_zz}

要将Livefyre Android SDK添加到Android studio中的项目，请执行以下操作：

1. 从GitHub获取最 [新的StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) 。
1. 从现有项目开始或创建新项目。
1. 右键单击您的项目并选择 **[!UICONTROL Open Module Settings]**。
1. 选择 **[!UICONTROL +]** 窗口左上角的按钮。
1. 选 **[!UICONTROL Import Existing Project.]** 择(在Android studio的新版本中，您可以在下 **[!UICONTROL Import Existing Project]** 找到 **[!UICONTROL More Modules]**。)

1. 浏览并选择StreamHub-Android-SDK。

Android studio可能会要求您将SDK转换为Gradle版本；如果出现这种情况，请选择 **[!UICONTROL next]** 然后 **[!UICONTROL finish]**。

转到项 **目文件夹&gt; app folder &gt; build.gradle** file under dependencies，以添加以下依赖关系：

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

确保以下代码行位于项目文 **件夹&gt; settings.gradle文件** :

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>您可以从Config.java中自定义配置。

## 客户 {#section_yfq_blv_zz}

StreamHub Android SDK公开了几个可用于请求Livefyre API端点的客户端类：

* **AdminClient** 为用户信息、密钥和其他元数据交换用户身份验证令牌。

* **BootstrapClient** 获取有关特定集合的最新内容和元数据。

* **StreamClient** 轮询集合的流以检索新的、更新的和删除的内容。

* **WriteClient** Post、标志和集合中的类似内容。

