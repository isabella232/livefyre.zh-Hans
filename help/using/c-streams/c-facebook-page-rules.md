---
description: 您可以创建从Facebook页面提取内容的流规则。
seo-description: 您可以创建从Facebook页面提取内容的流规则。
seo-title: Facebook页面规则
solution: Experience Manager
title: Facebook页面规则
uuid: 2be63476-1a92-409d-a22f-e1ec66b6dcc8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# Facebook页面规则{#facebook-page-rules}

您可以创建从Facebook页面提取内容的流规则。

您可以使用Facebook页面规则从Facebook页面流化公开发布的内容。 内容将以与SocialSync相同的频率拖入应用程序或文件夹，SocialSync会根据Facebook页面和帖子流量模式进行更改。 还支持Facebook页面中的链接，并将在流中显示。

要创建Facebook页面规则以将内容从Facebook页面拉入您的应用程序或文件夹，您可以按以下方式进行筛选：

* **[!UICONTROL Facebook Page]**

   * 输入&#x200B;**[!UICONTROL Name]**&#x200B;作为页面。 仅输入URL的尾随文本。 **例如：要** 添加内容， `https://facebook.com/KellysSuperFunFanPage`请在字 ** 段中键入KellysSuperFunFanPag **[!UICONTROL Name]** 。

   * 如果希望将用户评论加入页面帖子，请将&#x200B;**[!UICONTROL Include Facebook Comments for each post]**&#x200B;切换为开。
   * 如果希望从其他用户中排除帖子，请将&#x200B;**[!UICONTROL Only Show Author Posts]**&#x200B;切换为开。

有关所有流规则的其他流规则选项，请参阅[所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。

>[!NOTE]
>
>Livefyre仅限于从Facebook收到的内容，因此无法保证Facebook页面上的每个帖子都会包含在您的流中。

>[!NOTE]
>
>如果为特定Facebook页面启用Facebook SocialSync和Facebook页面规则，并为Facebook页面规则启用用户评论，则流规则将覆盖SocialSync。 内容将仅根据Facebook页面特定规则（而不是使用SocialSync）流式传输到应用程序中。

Facebook页面特选支持的内容类型包括：

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

