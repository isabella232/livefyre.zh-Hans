---
description: 'null'
seo-description: 'null'
seo-title: 幻灯片自定义
solution: Experience Manager
title: 幻灯片自定义
uuid: 99f8b697-4aa3-4813-bcac-d0 e0 bdee252 d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# 幻灯片自定义{#filmstrip-customizations}

所有应用程序使用 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 选项 **[!UICONTROL App Designer]**。有关 **[!UICONTROL Style]****[!UICONTROL Config]** 在 **[!UICONTROL App Designer.]**

您可以使用App Designer中的以下其他选项自定义幻灯片：

* **[!UICONTROL Content fit]**. 选择 **[!UICONTROL crop]** 裁剪内容以填充卡或 **[!UICONTROL Aspect Ratio]** 在卡片中显示整个图像(无论是否填满整个卡)。
* **[!UICONTROL Tile Size]**. 输入拼贴的大小(以像素为单位)。
* **[!UICONTROL Show Notifications]**. 选择当新内容流入Filmstrip应用程序时显示新内容的通知。
* **[!UICONTROL Require rights]**. 启用此选项可仅显示权限请求状态为“已授权”的内容。
* **[!UICONTROL Hide social branding when rights granted]** 在为某一内容授予权限时，切换开启以删除原始社交媒体网络(Twitter或Instagram)的标志。
* **[!UICONTROL Call-to-action button]** 您可以使用带有产品目录的呼叫行动按钮将用户定向到产品或您的站点进行进一步操作。

   * **[!UICONTROL Call-to-action button]** 切换切换以显示行动动员按钮。
   * **[!UICONTROL Require rights to display products]** 切换切换以要求内容所有者在为内容显示行动动员按钮之前为内容授予权限。

      >[!NOTE]
      >
      >即使未为内容授予权限，也会显示内容，但除非授予内容权限，否则调用操作按钮将不会显示内容。

   * **[!UICONTROL Show call-to-action in tile]**. 选择在站点访问者单击卡并在较大窗口中打开内容时，是否显示“幻灯片”拼贴上的行动号召按钮而不是显示行动动员按钮。
   * **[!UICONTROL Call-to-action indication text]** 要显示的文本，提示用户单击卡以打开行动动员模式。
   * **[!UICONTROL Call-to-action header text]** 要在内容模态中的调用操作按钮上方的标题中显示的词。默认文本是“Shop these products：.
   * **[!UICONTROL Call-to-action button text]** 要在内容模态中的调用操作按钮中显示的词。默认文本为“立即购买：.
   * **[!UICONTROL Product display options]** 选择是否要显示和 **[!UICONTROL Photo]****[!UICONTROL Product name]** 使用行动动员按钮。

      >[!NOTE]
      >
      >照片和产品名称按钮在启用时突出显示蓝色。

   * **[!UICONTROL Product URL referral tracking]** 切换切换以跟踪从此应用程序到关联产品页面的引用。
   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从应用程序内容到关联产品页面的引用跟踪。

* **[!UICONTROL Embed App in multiple pages]**.

   * **[!UICONTROL Filter UGC by Product ID]**. 选择此选项可为多个产品页面创建一个应用程序。将特定于产品的UGC用于每个产品页面的应用程序。您可以选择一个或多个文件夹，将特定集合关联到应用程序。
   * **[!UICONTROL Select product folders]**. 选择用于筛选UGC的顶级产品文件夹。使用CTRL/Command+单击可选择多个文件夹。Livefyre使用该文件夹确定该文件夹中要显示在各种页面上的应用程序中的产品。
   * **[!UICONTROL Show related content]**. 切换此操作以显示发布到应用程序的内容，但标记为其他产品ID。在用于应用程序显示的产品特定内容之后，Livefyre会显示其他产品和未与产品关联的内容的内容。Livefyre首先优先使用相同产品ID，然后使用其他产品ID发布到应用程序的内容，然后使用没有产品ID的应用程序发布到应用程序。

有关如何使用Livefyre. js自定义Filmstrip的更多信息，请参阅 [“幻灯片选项”](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) 。

