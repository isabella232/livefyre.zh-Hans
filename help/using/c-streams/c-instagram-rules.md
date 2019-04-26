---
description: 可创建从Instagram提取内容的流规则。
seo-description: 可创建从Instagram提取内容的流规则。
seo-title: Instagram规则
title: Instagram规则
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Instagram规则{#instagram-rules}

可创建从Instagram提取内容的流规则。

>[!NOTE]
>
>在创建Instagram流之前，您必须将至少一个Instagram业务帐户添加到其中的 **[!UICONTROL Social Accounts]** 一部分 **[!UICONTROL Network Settings]**。有关如何配置Instagram帐户的详细信息，请参阅 [关于Instagram帐户](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

基于@提及或标记标记创建Instagram规则。

>[!NOTE]
>
>所有Instagram规则至少需要一个主题标签。为规则添加关键字和用户名将返回包含两个条目的内容。

要创建Instagram规则以将内容从Instagram源提取到应用程序或文件夹，请按以下条件过滤：

* **[!UICONTROL Words]**

   * 输入或 **[!UICONTROL hashtags]** 排除在Instagram流中。指定 **[!UICONTROL Contains]** 和 **[!UICONTROL Does not contain]** 字段的值将返回包含第一个图像且不包含第二个图像的图像。

   * 例如，输入 **[!UICONTROL Contains]** 关键字Gions、Posey和 **[!UICONTROL Does not contain]** Dodger将返回包含单词“Ginants”或“Posey”的所有帖子，但不会包含Dodger字样。

      >[!NOTE]
      >
      >Instagram规则将返回包含作者注释中列出的主题标记的帖子，该标记可能不会显示在流中。

* **[!UICONTROL Mentions]**

   * 输入 **[!UICONTROL @mentions]** 以拖入流或从流中排除。

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >您必须在Livefyre中设置Instagram业务帐户，才能在Instagram流规则中使用作者搜索。有关在Livefyre中设置Instagram业务帐户的详细信息，请 [参阅关于Instagram帐户](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

   * 输入 **[!UICONTROL @usernames]** 以拖入流。与 **@用户名关联的帐户** 必须是Instagram业务帐户。

   * 输入 **要** 从流中排除的@用户名。

* **[!UICONTROL Additional Filters]**

   * 选择是否要包括 **[!UICONTROL All Content]**、 **[!UICONTROL Videos Only]**或在流 **[!UICONTROL Photos Only]** 中。

有关所有流规则的其他流规则选项，请参阅 [所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
