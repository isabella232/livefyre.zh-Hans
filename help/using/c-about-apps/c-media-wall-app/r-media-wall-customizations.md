---
description: 更改Media Wall应用程序的大小、宽度和交互选项。
seo-description: 更改Media Wall应用程序的大小、宽度和交互选项。
seo-title: 媒体墙自定义
solution: Experience Manager
title: 媒体墙自定义
uuid: 79ait92-3937-4bb4-a1 a6-b090 fb39 afb0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 媒体墙自定义{#media-wall-customizations}

更改Media Wall应用程序的大小、宽度和交互选项。



媒体墙将实时图像和其他内容流化到实时社交墙中，从而可视化活动周围的所有活动。

如果启用此功能，用户可以将文本、图像或视频直接发布到此应用程序。支持的文件类型包括：

* 图像：JPEG、GIF、PNG
* 视频：Quicktime/MOV、MP4、MPEG、WebM
* 音频：WAV、Wave、X-MS-WMA、FAC、OGG、MPEG

* **[!UICONTROL Items to load]**

   设置显示的内容项目的初始数量。

* **[!UICONTROL Load content with animation.]** 打开此选项可在带有动画的页面上加载媒体墙。关闭此选项可在不带动画的页面上加载媒体墙。
* **[!UICONTROL Number of columns.]** 设置媒体墙的列数。无论窗口或浏览器的大小如何，列数都保持不变。如果选择“自动”，列数将调整以显示屏幕大小的优化列数。
* **[!UICONTROL Fit content to width]**. 当此选项关闭时，内容将裁剪为正方形。切换此选项可显示卡中的整个图像，无论是否填满整个卡。
* **[!UICONTROL Include content modal]**

   允许用户单击流中的照片，以在覆盖的弹出窗口中打开它。

* **[!UICONTROL Require rights]**. 启用此选项可仅显示权限请求状态为“已授权”的内容。
* **[!UICONTROL Hide social branding when rights granted]** 在为某一内容授予权限时，切换开启以删除原始社交媒体网络(Twitter或Instagram)的标志。

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. 选择是否允许用户使用上传按钮发布文本、照片或视频。
   * **[!UICONTROL Require Media]**. 切换到开启，要求用户使用“上传按钮”只上传照片或视频内容。
   * 您可以编辑以下“上传按钮”字段的默认文本：

      * **[!UICONTROL Upload Button Text]**. 上传按钮的文本。默认文本是“您要想什么？”
      * **[!UICONTROL Comment Modal Title]**. 用于发布内容的模态站点的标题。默认文本为“发布您的评论”。
      * **[!UICONTROL Comment Modal Button]**. 访客点击以发布内容的按钮站点文本。默认文本为“发布您的评论”。

* **[!UICONTROL Call-to-action button]** 您可以使用包含产品目录的“行动动员”按钮将用户定向到产品或您的站点进行进一步操作。

   * **[!UICONTROL Call-to-action button]** 切换切换以显示行动动员按钮。
   * **[!UICONTROL Require rights to display products]** 切换切换以要求内容所有者在为内容显示“行动动员”按钮之前为内容授予权限。

      >[!NOTE]
      >
      >即使未为内容授予权限，内容也会显示，但除非授予内容权限，否则“行动动员”按钮将不会显示内容。

   * **[!UICONTROL Call-to-action header text]** 要显示在内容模态中的行动动员按钮上方的标题中的词。默认措辞是：“购买这些产品：.
   * **[!UICONTROL Call-to-action button text]** 要在内容模态中的“行动动员”按钮中显示的词。默认文本为“立即购买：.
   * **[!UICONTROL Product display options]** 选择是否要使用“行动动员”按钮显示照片和产品名称。

      >[!NOTE]
      >
      >照片和产品名称按钮在启用时突出显示蓝色。

   * **[!UICONTROL Product URL referral tracking]** 切换切换以跟踪从此应用程序到关联产品页面的引用。
   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从应用程序内容到关联产品页面的引用跟踪。

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. 选择此选项可为多个产品页面创建一个应用程序。将特定于产品的UGC用于每个产品页面的应用程序。您可以选择一个或多个文件夹，将特定集合关联到应用程序。
   * **[!UICONTROL Select Product folders]**. 选择用于筛选UGC的顶级产品文件夹。使用CTRL/Command+单击可选择多个文件夹。Livefyre使用该文件夹确定该文件夹中要显示在各种页面上的应用程序中的产品。
   * **[!UICONTROL Show related content]**. 切换此操作以显示发布到应用程序的内容，但标记为其他产品ID。在用于应用程序显示的产品特定内容之后，Livefyre会显示其他产品和未与产品关联的内容的内容。Livefyre首先优先使用相同产品ID，然后使用其他产品ID发布到应用程序的内容，然后使用没有产品ID的应用程序发布到应用程序。

您可以使用以下方法自定义媒体墙：

* **[!UICONTROL Style]** 以及所有应用程序 **[!UICONTROL Config]** 的选项 **[!UICONTROL App Designer]**。有关中所有应用程序的标准 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 选项的详细信息，请参阅自定义应用程序 **[!UICONTROL App Designer]**。

* 集成工具。有关如何使用集成工具自定义媒体墙的更多信息，请参阅 [媒体墙集成](/help/implementation/c-app-integrations/c-media-wall-integration.md) 。

