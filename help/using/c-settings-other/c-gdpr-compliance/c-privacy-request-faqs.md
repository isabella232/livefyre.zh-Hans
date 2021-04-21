---
description: 有关GDPR就绪的隐私请求的常见问题解答(FAQ)。
title: 隐私请求常见问题解答
exl-id: 6d0add45-589a-46d0-b15a-63a7599aad73
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 1%

---

# 隐私请求常见问题解答{#privacy-request-faqs}

有关GDPR就绪的隐私请求的常见问题解答(FAQ)。

* **如何在使选择退出用Livefyre应用程序的站点上跟踪站点访客?** 当站点访客选择退出时，客户实施必须向Livefyre表明用户已选择退出，然后才能实例化应用程序。Livefyre已经使用JavaScript选项`userPrivacyOptOut`创建了实现此目的的方法。 有关如何使用`userPrivacyOptOut`的详细信息，请参阅[userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md)。

   当`userPrivacyOptOut`标志设置为true时，页面上的任何应用程序都不会通过使用cookie或其他方法将数据传输到Livefyre服务器。 然后，Livefyre将不会使用可用于跟踪站点存储的数据更新本地访客。 如果源不支持代理，则除非用户单击视频并批准来自该源的潜在跟踪，否则Livefyre会在内容上显示一个蒙版。

   如果您使用Livefyre Identity，则用户可以选择删除其用户档案或为其用户帐户创建跟踪数据的报告。

* **如何防止从已选择退出的网站访客收集将来的内容？** 在使 `userPrivacyOptOut` 用 `livefyre.js` Livefyre应用程序的网页上使用。有关`userPrivacyOptOut`的详细信息，请参阅[userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md)。

* **如何为应用程序用户或社交帐户所有者生成报告并删除数据？** [隐私](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) 请求，以生成报告并从应用程序中删除用户数据。

* **如何删除访客的所有内容？** Livefyre不会保留有关站点访客的永久信息，但以Cookie形式除外，以便唯一标识这些站点，以实现LiveCount功能。Livecount是站点上的临时和实时访客计数。 在访客离开或清除Cookie后，不会保留任何历史记录。

   创建[隐私请求](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests)以删除帐户。 Livefyre会删除用户用户档案和任何相关记录，或将其设为匿名。

* **如何删除注册用户的内容？** 创建隐 [私](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) 请求以删除帐户。用户用户档案和任何相关记录将被完全销毁。

   >[!NOTE]
   >
   >此操作无法撤销。

* **如何生成当前或前员工跟踪的数据报表？** [视图隐私](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) 报表，以生成用户帐户跟踪的数据报表。

* **Livefyre社交流是否兼容？** 当用户从其社交网络中删除帖子或推文时，在24小时内，内容也会从Livefyre的所有源中删除。这适用于Twitter和Facebook。
