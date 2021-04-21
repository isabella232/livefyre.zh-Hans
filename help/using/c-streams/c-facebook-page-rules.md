---
description: 您可以创建从Facebook页面提取内容的流规则。
title: Facebook页面规则
exl-id: 1dc728c6-81fa-4c6c-acba-d9a4aea71ed2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# Facebook页面规则{#facebook-page-rules}

您可以创建从Facebook页面提取内容的流规则。

您可以使用Facebook页面规则流化Facebook页面中公开发布的内容。 内容将以与SocialSync相同的频率被拉入应用程序或文件夹中，SocialSync会根据Facebook页面和帖子流量模式进行更改。 facebook页面内的链接也受支持，并将显示在流中。

要创建Facebook页面规则以将Facebook页面的内容拉入您的应用程序或文件夹，您可以按以下方式进行筛选：

* **[!UICONTROL Facebook Page]**

   * 输入&#x200B;**[!UICONTROL Name]**&#x200B;作为页面。 仅输入URL的尾随文本。 **例如：要** 从中添加内 `https://facebook.com/KellysSuperFunFanPage`容，请 ** 在字段中键 **[!UICONTROL Name]** 入KellysSuperFunFanPag。

   * 如果希望将用户评论包含到页面帖子，请将&#x200B;**[!UICONTROL Include Facebook Comments for each post]**&#x200B;切换为开。
   * 如果希望从其他用户中排除帖子，请将&#x200B;**[!UICONTROL Only Show Author Posts]**&#x200B;切换为开。

有关所有流规则的其他流规则选项，请参阅[所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。

>[!NOTE]
>
>Livefyre仅限于从Facebook收到的内容，因此无法保证Facebook页面上的每个帖子都将包含在您的流中。

>[!NOTE]
>
>如果为特定的Facebook页面启用了Facebook SocialSync和Facebook页面规则，并且为Facebook页面规则启用了用户注释，则流规则将覆盖SocialSync。 内容将仅基于Facebook页面特选规则（而不是使用SocialSync）流式传输到应用程序中。

facebook Page Curate支持的内容类型包括：

* 页面所有者或管理员

   * 状态
   * 照片
   * 视频作为链接

* 标准Facebook用户

   * 状态
   * 照片
   * 视频作为链接

* 第三方

   * 状态
