---
description: 在Livefyre中创建隐私请求。
title: 创建隐私请求
exl-id: 117e1edb-becd-45f2-bfe5-12fb19ad01e0
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---

# 创建隐私请求{#create-a-privacy-request}

在Livefyre中创建隐私请求。

删除用户的所有数据，为用户生成所有数据的报告，并使用此过程进行选择加入或选择退出更改。

要搜索和查找用户并生成其内容的报表，请执行以下操作：

1. 转至&#x200B;**[!UICONTROL Settings > Privacy]**，然后单击&#x200B;**[!UICONTROL Create Request]**。

   ![](assets/privacypage1.png)

1. 在&#x200B;**[!UICONTROL Submit Request]**&#x200B;窗口中填写信息：

   * **[!UICONTROL Reference Id]**。输入要用于将来引用的标识符。 例如，您可以添加最多255个字符的文本、票证号、URL、电子邮件地址或其他字符串
   * **[!UICONTROL Type]**

      * **访问**. 收集与帐户关联的所有可用数据。 敏感详细信息（例如密码或社交凭据）将被模糊处理或忽略。

      * **删除**. 取消显示或模糊化与帐户关联的所有数据。 **如果选择此选项并单击提交，则无法撤消或取消此操作，也 *无法恢复已删除的数据。*** 如果帐户属于Livefyre Studio用户，将保留一些数据以保持业务记录的完整性。

         >[!IMPORTANT]
         >
         >删除帐户的数据将永久删除或销毁与该帐户关联的数据。 您无法撤消此操作，也无法在删除数据后恢复数据。

      * **选择退出**。防止Livefyre通过流或社交搜索被动地从社交帐户收集数据或内容。 选择加入和选择退出不适用于注册用户
      * **选择加入**。使Livefyre能够被动地从某个之前通过流或社交搜索选择退出的社交帐户收集数据或内容。 选择加入和选择退出不适用于注册用户

      ![](assets/privacypage2.png)

   * **[!UICONTROL Identifier Type]** 和 **[!UICONTROL Identifier]**

      * **[!UICONTROL User Account]**

         * 通过用户管理系统或Livefyre的Studio用户标识符生成的用户帐户ID标识注册用户的帐户。 您还可以在&#x200B;**Livefyre****用户设置**&#x200B;的用户详细信息中或在&#x200B;**资产库**&#x200B;或&#x200B;**应用程序内容**&#x200B;中的内容详细信息中找到用户帐户ID

         * 允许的值：最多255个字符的字母数字字符串。 电子邮件地址不是有效输入
      * **[!UICONTROL Facebook User]**

         * 通过Facebook提供的数字ID标识帐户。 请求者应提供此内容。 您可以在此处](https://www.facebook.com/help/1397933243846983?helpref=faq_content)找到如何定位数字Facebook ID [的说明
         * 允许的值：6-16个数字字符
      * **[!UICONTROL Instagram User]**

         * 通过Instagram提供的数字ID标识帐户。 请求者应提供此内容。 您可以通过联机搜索找到有关如何在Instagram帐户上定位数字Instagram ID的说明
         * 允许的值：5-16个数字字符
      * **[!UICONTROL Twitter User]**

         * 通过Twitter提供的数字ID标识帐户。 请求更改隐私的人员应提供此信息。 您可以通过联机搜索找到有关如何查找Twitter帐户的数字Twitter ID的说明
         * 允许的值：5-16个数字字符
      * **[!UICONTROL YouTube User]**

         * 通过YouTube提供的数字ID标识帐户。 请求更改隐私的人员应提供此信息。 您可以在[此处](https://support.google.com/youtube/answer/3250431?hl=en)找到有关如何在YouTube帐户上查找数字YouTube ID的说明
         * 允许的值：5-16个数字字符
      * **[!UICONTROL Generic Author]**

         * 通过Livefyre作者ID(JID)标识帐户。 对于通过RSS、Tumblr或URL来源的内容，请使用此选项。 要查找此ID，请在&#x200B;**App Content**&#x200B;或&#x200B;**Asset Library**&#x200B;中搜索归属于作者的内容，然后选择一个项目。 此ID位于&#x200B;**Info**&#x200B;下的&#x200B;**App Content**&#x200B;中，或位于&#x200B;**Details**&#x200B;部分&#x200B;**Author**&#x200B;下的&#x200B;**资产库**&#x200B;中

         * 允许的值：最多255个字符的字母数字字符串

         ![](assets/privacypage3.png)








1. 单击 **[!UICONTROL Finish]**.

   ![](assets/privacypage4.png)

1. （仅限“删除请求”）确认要删除用户的所有信息。

   >[!IMPORTANT]
   >
   >删除帐户的数据将永久删除或销毁与该帐户关联的数据。 您无法撤消此操作，也无法在删除数据后恢复数据。
