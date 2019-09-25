---
description: 更改媒体墙应用程序的大小、宽度和交互选项。
seo-description: 更改媒体墙应用程序的大小、宽度和交互选项。
seo-title: 媒体墙自定义
solution: Experience Manager
title: 媒体墙自定义
uuid: 79aecd92-3937-4bb4-a1a6-b090fb39afb0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 媒体墙自定义{#media-wall-customizations}

更改媒体墙应用程序的大小、宽度和交互选项。



媒体墙将实时图像和其他内容流式传输到实时社交墙中，从而可视化活动周围的所有活动。

如果启用，用户可以直接将文本、图像或视频发布到此应用程序。 受支持的文件类型包括：

* 图像：JPEG、GIF、PNG
* 视频：Quicktime/MOV、MP4、MPEG、WebM
* 音频：WAV、WAVE、X-MS-WMA、FLAC、OGG、MPEG

* **[!UICONTROL Items to load]**

   设置显示的内容项目的初始数量。

* **[!UICONTROL Load content with animation.]** 打开此选项，在具有动画的页面上加载媒体墙。 关闭此选项可在没有动画的页面上加载媒体墙。
* **[!UICONTROL Number of columns.]** 设置媒体墙的列数。 列数保持不变，而与窗口或浏览器的大小无关。 如果选择“自动”，则列数将调整为根据屏幕大小显示优化的列数。
* **[!UICONTROL Fit content to width]**. 关闭此选项后，内容会被裁剪为正方形。 将此选项切换为打开，以在卡中显示整个图像，无论是否填满整个卡。
* **[!UICONTROL Include content modal]**

   允许用户单击流中的照片以在叠加的弹出窗口中打开它。

* **[!UICONTROL Require rights]**. 启用此选项可仅显示权限请求状态为“已授权”的内容。
* **[!UICONTROL Hide social branding when rights granted]** 打开此按钮可在授予某条内容的权限时删除源社交媒体网络（Twitter或Instagram）的徽标。

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. 选择是否允许用户使用上传按钮发布文本、照片或视频。
   * **[!UICONTROL Require Media]**. 切换到开启状态，以要求用户仅使用“上传”按钮上传照片或视频内容。
   * 您可以编辑以下“上传按钮”字段的默认文本：

      * **[!UICONTROL Upload Button Text]**. “上传”按钮的文本。 默认文本为“您在想什么？”
      * **[!UICONTROL Comment Modal Title]**. 模态网站访客用于发布内容的标题。 默认文本为“发布您的评论”。
      * **[!UICONTROL Comment Modal Button]**. 按钮站点访客单击以发布内容的文本。 默认文本为“发布您的评论”。

* **[!UICONTROL Call-to-action button]** 您可以将行动动员按钮与产品目录一起使用，以将用户定向到产品或您的站点以进一步执行操作。

   * **[!UICONTROL Call-to-action button]** 切换至开启以显示行动动员按钮。
   * **[!UICONTROL Require rights to display products]** 切换为打开，以要求内容所有者已授予内容权限，然后才会为内容显示行动动员按钮。

      >[!NOTE]
      >
      >即使未授予内容权限，内容也会显示，但除非授予内容权限，否则行动动员按钮将不显示内容。

   * **[!UICONTROL Call-to-action header text]** 内容模式中行动动员按钮上方标题中显示的词语。 默认措辞为“Shop these products:”。
   * **[!UICONTROL Call-to-action button text]** 要在内容模式的“行动动员”按钮中显示的词。 默认文本为“立即购买：”。
   * **[!UICONTROL Product display options]** 选择是否要使用行动动员按钮显示照片和产品名称。

      >[!NOTE]
      >
      >“照片”和“产品”名称按钮在启用时均突出显示为蓝色。

   * **[!UICONTROL Product URL referral tracking]** 切换至开启以跟踪从此应用程序到关联产品页面的引用。
   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从应用程序内容到关联产品页面的引用跟踪。

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. 选择此选项可为多个产品页面创建一个应用程序。 将特定于产品的UGC过滤为每个产品页面的应用程序。 您可以选择一个或多个文件夹，将特定集合关联到应用程序。
   * **[!UICONTROL Select Product folders]**. 选择要用于筛选UGC的顶级产品文件夹。 使用CTRL/Command +单击可选择多个文件夹。 Livefyre使用该文件夹确定该文件夹中要在不同页面上的应用程序中显示的产品。
   * **[!UICONTROL Show related content]**. 切换此选项可显示已发布到应用程序但使用其他产品ID标记的内容。 显示应用程序的特定产品内容后，Livefyre将显示其他产品的内容以及与某个产品无关的内容。 Livefyre首先使用相同的产品ID优先安排内容的优先级，然后使用其他产品ID发布到应用程序的内容，然后发布到没有产品ID的应用程序的内容。

您可以使用以下方式自定义媒体墙：

* **[!UICONTROL Style]** 和中 **[!UICONTROL Config]** 所有应用程序的选项 **[!UICONTROL App Designer]**。 有关中所有应用程序的标准和选项的详细 **[!UICONTROL Style]** 信息， **[!UICONTROL Config]** 请参阅自定义应用程序 **[!UICONTROL App Designer]**。

* 集成工具。 有关如 [何使用集成工具自定义媒体墙的更多信息](/help/implementation/c-app-integrations/c-media-wall-integration.md) ，请参阅媒体墙集成。

