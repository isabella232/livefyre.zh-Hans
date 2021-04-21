---
description: 您可以创建从Instagram中提取内容的流规则。
title: Instagram规则
exl-id: ac00a12c-94b1-4464-ad3f-991382759d71
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Instagram规则{#instagram-rules}

您可以创建从Instagram中提取内容的流规则。

>[!NOTE]
>
>在创建Instagram流之前，您必须在&#x200B;**[!UICONTROL Network Settings]**&#x200B;的&#x200B;**[!UICONTROL Social Accounts]**&#x200B;部分至少添加一个Instagram业务帐户。 有关如何配置Instagram帐户的详细信息，请参阅[关于Instagram帐户](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

基于@mentions或井号标签创建Instagram规则。

>[!NOTE]
>
>所有Instagram规则都至少需要一个主题标签。 为规则添加关键字和用户名将返回包含这两个条目的内容。

要创建Instagram规则以将内容从Instagram源拉入您的应用程序或文件夹，请按以下方式进行筛选：

* **[!UICONTROL Words]**

   * 输入&#x200B;**[!UICONTROL hashtags]**&#x200B;以包含在或从Instagram流中排除。 为&#x200B;**[!UICONTROL Contains]**&#x200B;和&#x200B;**[!UICONTROL Does not contain]**&#x200B;字段指定值将返回包含第一个字段且不包含第二个字段的图像。

   * 例如，输入&#x200B;**[!UICONTROL Contains]**&#x200B;关键字Giants、Posey和&#x200B;**[!UICONTROL Does not contain]**&#x200B;关键字Dodger将返回所有包含“Giants”或“Posey”的帖子，但不包括“Dodger”。

      >[!NOTE]
      >
      >Instagram规则将返回帖子，这些帖子在作者的评论中包含列出的主题标记，这些标记可能不显示在流中。

* **[!UICONTROL Mentions]**

   * 输入&#x200B;**[!UICONTROL @mentions]**&#x200B;以拉入流，或从流中排除。

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >您必须在Livefyre中设置了Instagram业务帐户，才能在Instagram流规则中使用作者搜索。 有关在Livefyre中设置Instagram业务帐户的详细信息，请参阅[关于Instagram帐户](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

   * 输入&#x200B;**[!UICONTROL @usernames]**&#x200B;以拉入流。 与&#x200B;**@username**&#x200B;关联的帐户必须是Instagram业务帐户。

   * 输入要从流中排除的&#x200B;**@usernames**。

* **[!UICONTROL Additional Filters]**

   * 选择是要在流中包含&#x200B;**[!UICONTROL All Content]**、**[!UICONTROL Videos Only]**&#x200B;还是&#x200B;**[!UICONTROL Photos Only]**。

有关所有流规则的其他流规则选项，请参阅[所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
