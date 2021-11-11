---
description: 了解如何将LivefyreExperience Manager与Hootsuite结合使用，从而允许您直接从Hootsuite功能板管理、管理和共享用户生成的内容。
title: 将Adobe Experience Manager Livefyre与Hootsuite结合使用
exl-id: 1ca84c72-95ec-485d-9c8e-ace4487225d6
source-git-commit: ecac8943330cc0dd8ae3ce0ba4ba66948c502b9e
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 1%

---

# 将Adobe Experience Manager Livefyre与Hootsuite结合使用{#use-adobe-experience-manager-livefyre-with-hootsuite}

了解如何将LivefyreExperience Manager与Hootsuite结合使用，从而允许您直接从Hootsuite功能板管理、管理和共享用户生成的内容。

## 将Adobe Experience Manager Livefyre与Hootsuite结合使用 {#topic_FB6E613DBCF74F39ABD5045C501EA326}

了解如何将LivefyreExperience Manager与Hootsuite结合使用，从而允许您直接从Hootsuite功能板管理、管理和共享用户生成的内容。

## 入门指南 {#task_22699BD901C24384AB2DC02D926D8F4A}

任务上下文

1. 从Hootsuite应用程序目录安装适用于Hootsuite的Adobe Experience Manager Livefyre。

1. 在您的“Hootsuite”功能板中，单击 **使用Adobe登录**.

   ![](assets/hootsuite-login.png)

1. 使用您的Livefyre凭据登录Experience ManagerLivefyre 。
1. 单击 **授权** 授予Hootsuite访问库的权限。

   ![](assets/hootsuite-authorize.png)

   授予权限后，您将返回到Hootsuite功能板，您可以在该功能板中搜索Experience ManagerLivefyre库中的资产。

## 搜索资产 {#task_0B011B0C539E400BB72A6DF69FBF66C0}

任务上下文

1. 单击菜单栏中的搜索图标，以在您的Experience ManagerLivefyre库中搜索资产。

   ![](assets/hootsuite-search.png)

1. 单击 **选择** 此时，将显示一个弹出窗口，其中包含您的所有库。
1. 单击库的文件夹，然后单击 **选择文件夹** ，以选择将在您的Hootsuite流中显示的库。

   ![](assets/hootsuite-select.png)

## 筛选选项 {#concept_5D062A9CD61A4B2E90784E5AA31CB16D}

您可以使用显示资产的来源、权限、关键字和标记部分来筛选搜索结果。

![](assets/hootsuite-filters.png)

筛选选项包括：

| 区域 | 描述 |
|--- |--- |
| 资产显示来源 | 选择以从所有源或从单个源查看资产。 例如：Instagram、Twitter、Facebook等 |
| 权限 | 选择以仅查看具有特定权限设置的资产。 |
| 关键字 | 选择以按“关键词”或“标记”过滤结果。 按关键词过滤将搜索帖子的文本内容以及作者显示名称和作者用户名。 |
| 标记 | 选择以按“关键词”或“标记”过滤结果。 按关键词过滤将搜索帖子的文本内容以及作者显示名称和作者用户名。 |

选择搜索参数后，搜索时，您的资产将以流形式显示：

![](assets/hootsuite-stream.png)

### 流菜单选项

单击用户名或图标将显示相应网络上的用户。 单击时间将显示原始文章。 当鼠标悬停在项目上时，将显示更多选项。 单击共享 ![](assets/share.png)

图标会将当前资产添加到网络组合框，以便您通过Hootsuite与网络共享该资产。

>[!NOTE]
>
>仅当您筛选具有已授予权限的资产时，才会显示“共享”按钮。

单击“分配”  ![](assets/assign.png) 图标，以将当前项目分配给您的Hootsuite团队成员之一。 如果已分配某个项目，则 ![](assets/resolve.png) 图标。 单击它可解析当前分配。

### 其他应用程序菜单

单击设置  ![](assets/settings.png) 图标将允许您断开当前Experience ManagerLivefyre帐户的连接，并与另一个帐户连接。

单击菜单  ![](assets/menu.png) 图标将显示此文档、支持和Synaptive网站的链接。

## Experience ManagerLivefyre应用程序插件 {#task_33C8CEF4F5E44830B970BB3A7AAA2AA6}

除了能够在Hootsuite流中显示资产库外，您还可以将来自Instagram、Twitter、Facebook和YouTube流的项目保存到Experience ManagerLivefyre库。

1. 单击位于每个项目底部的菜单图标。

   ![](assets/hootsuite-menu-icon.png)

1. 选择 **发送到AEM Livefyre**.
1. 选择一个或多个要将资产保存到的库。

   ![](assets/hootsuite-save.png)

1. 单击 **保存到库**，则该项目将会保存到您选择的库中。

## Experience ManagerLivefyre Media Library组件 {#task_9CA2D5D49F8E463F9EF475BC09C8ACC9}

您可以通过报表包编辑器的媒体组件访问您的资产。

1. 在编辑器中，单击 **打开Media Library** 链接 **媒体** 中。

   ![](assets/hootsuite-open-media-library.png)

1. 从下拉菜单中选择Adobe Experience Manager Livefyre，此时将显示您的文件。

   ![](assets/hootsuite-aem-files.png)

1. 要将资产添加到您正在撰写的当前帖子，请单击该资产。 要搜索特定资产，请在 **搜索媒体** 框中，将显示结果。
