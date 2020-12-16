---
description: 了解权限请求的工作方式。 将用户生成的内容(UGC)引入Livefyre应用程序时，该内容包含重用的默许权限。 您必须获得作者的许可才能使用Twitter或Instagram中的内容。
seo-description: 了解权限请求的工作方式。 将用户生成的内容(UGC)引入Livefyre应用程序时，该内容包含重用的默许权限。 您必须获得作者的许可才能使用Twitter或Instagram中的内容。
seo-title: 请求权限
title: 请求权限
uuid: d3194afa-f3c6-44ed-b03f-9b1ecb50c1d3
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---


# 请求权限{#requesting-rights}

了解权限请求的工作方式。 将用户生成的内容(UGC)引入Livefyre应用程序时，该内容包含重用的默许权限。 您必须获得作者的许可才能使用Twitter或Instagram中的内容。

库、应用程序内容、ModQ和AEM Commerce中提供以下权限状态：

* **[!UICONTROL Granted]**。当作者授予您重用其内容的权利时，资产的状态将变为&#x200B;**[!UICONTROL Granted]**。

* **[!UICONTROL Expired]**。Livefyre会监视Instagram和Twitter流，以供作者回复14天。 14天后，请求将过期，权限请求状态将更改为&#x200B;**[!UICONTROL Expired]**，您可以再发送一个请求或从库中删除项目。
* **[!UICONTROL Requested]**。从库请求内容权限。 您一次可以对一个或多个资产执行此操作。 在您请求权限后，Livefyre会将资产状态设置为&#x200B;**[!UICONTROL Requested]**。
* **[!UICONTROL Needs Review]**。如果作者回复的注释不包含#approvalHash标记，则资产的状态将变为&#x200B;**[!UICONTROL Needs Review]**。

* **[!UICONTROL Request Failed]**。无法发送请求（由于过期的令牌等）。
* **[!UICONTROL Request Pending]**。将权限请求排入队列，以便一次不发送过多请求。

您可以请求对从Twitter和Instagram获取的资产的权限。 您必须将资产保存到库中才能请求权限。

您必须配置&#x200B;*Instagram商业帐户*，以使用部分自动化的工作流从Instagram请求资产权限。

您只能对通过业务帐户搜索或流搜索获得的内容使用此功能。 要请求您从个人Instagram帐户获得的内容的权限，您必须手动发送权限请求。

>[!NOTE]
>
>有关不同类型的Instagram帐户以及如何使用它们的详细信息，请参阅[关于Instagram帐户](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。 有关如何请求Instagram帐户权限的信息，请参阅[发送手动权限请求](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md#c_send_instagram_manual_rights_request)和[发送部分自动权限请求](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md#c_send_an_instagram_rights_request_from_the_library)。

