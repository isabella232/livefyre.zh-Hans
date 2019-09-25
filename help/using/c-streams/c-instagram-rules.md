---
description: 您可以创建从Instagram中提取内容的流规则。
seo-description: 您可以创建从Instagram中提取内容的流规则。
seo-title: Instagram规则
title: Instagram规则
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Instagram规则{#instagram-rules}

您可以创建从Instagram中提取内容的流规则。

>[!NOTE]
>
>在创建Instagram流之前，您必须至少在中的部分添加一个Instagram **[!UICONTROL Social Accounts]** 业务帐户 **[!UICONTROL Network Settings]**。 有关如何配置Instagram帐户的详细信息，请参阅关于 [Instagram帐户](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

根据@mentions或主题标签创建Instagram规则。

>[!NOTE]
>
>所有Instagram规则都至少需要一个主题标签。 为规则添加关键字和用户名将返回包含这两个条目的内容。

要创建Instagram规则以将Instagram源中的内容拉入您的应用程序或文件夹，请按以下方式过滤：

* **[!UICONTROL Words]**

   * 输 **[!UICONTROL hashtags]** 入以包含在Instagram流中或从Instagram流中排除。 为和字段指定 **[!UICONTROL Contains]** 值 **[!UICONTROL Does not contain]** 将返回包含第一个且不包含第二个的图像。

   * 例如，输入 **[!UICONTROL Contains]** 关键字Giants、Posey和关键字 **[!UICONTROL Does not contain]** Dodger将返回所有包含单词Giants或Posey的帖子，但不包括单词Dodger。

      >[!NOTE]
      >
      >Instagram规则将返回在作者评论中包含列出的主题标签的帖子，这些主题标签可能不显示在流中。

* **[!UICONTROL Mentions]**

   * 输入 **[!UICONTROL @mentions]** 以拉入流，或从流中排除。

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >您必须在Livefyre中设置Instagram商业帐户，才能在Instagram流规则中使用作者搜索。 有关在Livefyre中设置Instagram业务帐户的更多信息，请参 [阅关于Instagram帐户](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

   * 进入 **[!UICONTROL @usernames]** 以拉入流。 与@username关联的帐 **户必须是Instagram商业帐户** 。

   * 输入要 **从流中排除的** @usernames。

* **[!UICONTROL Additional Filters]**

   * 选择是要包含、 **[!UICONTROL All Content]**&#x200B;还 **[!UICONTROL Videos Only]**&#x200B;是 **[!UICONTROL Photos Only]** 在流中。

有关所有流规则的其他流规则选项，请参 [阅所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
