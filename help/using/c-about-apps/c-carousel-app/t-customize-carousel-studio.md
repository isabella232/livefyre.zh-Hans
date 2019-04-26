---
description: 更改传送应用程序的大小、宽度和交互选项。
seo-description: 更改传送应用程序的大小、宽度和交互选项。
seo-title: 使用Studio自定义传送
solution: Experience Manager
title: 使用Studio自定义传送
uuid: 24f080fc-37ff-40d4-8c1a-a502 ee8 ac978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 使用Studio自定义传送{#customize-a-carousel-using-studio}

更改传送应用程序的大小、宽度和交互选项。

所有应用程序使用 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 选项 **[!UICONTROL App Designer]**。有关中所有应用程序的标准 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 选项的详细信息，请参阅自定义应用程序 **[!UICONTROL App Designer]**。

您可以使用App Designer中的以下其他选项自定义传送：

* **[!UICONTROL Max Number of Items]**

   设置要在传送中显示的项目数。默认值为50。

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. 仅适用于计算机屏幕

   * 如果内容大于600像素，则水平显示
   * 如果内容小于600像素，则垂直显示
   * **垂直。** 适用于计算机屏幕或移动设备。在移动设备中，卡会收缩以适合屏幕大小。

* **[!UICONTROL Call-to-action button]** 您可以使用包含产品目录的“行动动员”按钮将用户定向到产品或您的站点进行进一步操作。

   * **[!UICONTROL Call-to-action button]** 切换切换以显示行动动员按钮。
   * **[!UICONTROL Require rights to display products]** 切换切换以要求内容所有者在为内容显示行动动员按钮之前为内容授予权限。
   >[!NOTE]
   >
   >即使未为内容授予权限，也会显示内容，但除非授予内容权限，否则调用操作按钮将不会显示内容。

   * **[!UICONTROL Show call-to-action in tile]**. 选择在站点访问者单击卡并在较大窗口中打开内容时，在拼贴上显示调用操作按钮而不是显示行动动员按钮。
   * **[!UICONTROL Call-to-action indication text]** 要显示的文本，提示用户单击卡以打开行动动员模式。
   * **[!UICONTROL Call-to-action header text]** 要显示在内容模态中的行动动员按钮上方的标题中的词。默认文本是“Shop these products：.
   * **[!UICONTROL Call-to-action button text]** 要在内容模态中的“行动动员”按钮中显示的词。默认文本为“立即购买：.
   * **[!UICONTROL Product display options]** 选择是否要显示和 **[!UICONTROL Photo]****[!UICONTROL Product name]** 使用行动动员按钮。
   >[!NOTE]
   >
   >照片和产品名称按钮在启用时突出显示蓝色。

   * **[!UICONTROL Product URL referral tracking]** 切换切换以跟踪从此应用程序到关联产品页面的引用。
   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从应用程序内容到关联产品页面的引用跟踪。



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. 选择此选项可为多个产品页面创建一个应用程序。将特定于产品的UGC用于每个产品页面的应用程序。您可以选择一个或多个文件夹，将特定集合关联到应用程序。
   * **[!UICONTROL Select Product folders]**. 选择用于筛选UGC的顶级产品文件夹。使用CTRL/Command+单击可选择多个文件夹。Livefyre使用该文件夹确定该文件夹中要显示在各种页面上的应用程序中的产品。
   * **[!UICONTROL Show related content]**. 切换此操作以显示发布到应用程序的内容，但标记为其他产品ID。在用于应用程序显示的产品特定内容之后，Livefyre会显示其他产品和未与产品关联的内容的内容。Livefyre首先优先使用相同产品ID，然后使用其他产品ID发布到应用程序的内容，然后使用没有产品ID的应用程序发布到应用程序。
