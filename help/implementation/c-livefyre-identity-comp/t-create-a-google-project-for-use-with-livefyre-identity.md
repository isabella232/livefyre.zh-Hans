---
description: 您可以将Livefyre Identity与Google结合使用，允许用户使用Google登录，与您网站上的App交互。
seo-description: 您可以将Livefyre Identity与Google结合使用，允许用户使用Google登录，与您网站上的App交互。
seo-title: 创建Google项目以用于Livefyre Identity
solution: Experience Manager
title: 创建Google项目以用于Livefyre Identity
uuid: b0a6bb8a-abEA-4f5 c-92ed-026e60183 e1 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 创建Google项目以用于Livefyre Identity{#create-a-google-project-for-use-with-livefyre-identity}

您可以将Livefyre Identity与Google结合使用，允许用户使用Google登录，与您网站上的App交互。

为了允许用户使用他们的Google凭据登录，Livefyre需要以下Google项目信息：

* 客户端ID
* 客户端机密

要创建用于Livefyre Identity的Google Project，请执行以下操作：

1. 转到 [https://console.cloud.google.com/project](https://console.cloud.google.com/project) 并登录到您的Google帐户以创建新的应用程序，或选择现有的应用程序以用于Livefyre Identity。
1. 从应用程序的项目控制板中，单击 **[!UICONTROL Enable and Manage APIs]**。
1. 在API概述页面的Social API下，单击以启用Google+ API。
1. 从API凭据页面中，选择 **[!UICONTROL Credentials > New credentials > OAuth]** 客户端ID。在打开的 **[!UICONTROL Create client ID]** 页面中：

   * 选择应用程序类型：Web应用程序。
   * 输入for **[!UICONTROL Name]** the **[!UICONTROL Client ID]**.
   * **[!UICONTROL Authorized JavaScript origins]** 将字段留空。
   * 输入 **[!UICONTROL Authorized redirect URIs]**： `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/google_fyre` (在这里 **[!UICONTROL {networkName}]** ，您的Livefyre提供了网络名称。例如：** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**)
   * 单击 **[!UICONTROL Create]** 以保存凭据。

完成后，Google的API管理器&gt;凭据页面将列出项目的客户端ID和客户端机密，以便在Studio的集成设置页面中使用。
