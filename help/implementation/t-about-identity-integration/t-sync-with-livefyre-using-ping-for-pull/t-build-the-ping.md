---
description: 构建ping，以便在用户更新其用户档案时，您的页面ping Livefyre。
seo-description: 构建ping，以便在用户更新其用户档案时，您的页面ping Livefyre。
seo-title: 构建Ping
solution: Experience Manager
title: 构建Ping
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: f76dcd31e58b94856bf551009c2ac50c3233e516
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# 生成Ping{#build-the-ping}

构建ping，以便在用户更新其用户档案时，您的页面ping Livefyre。

当Livefyre收到`networkName`和`user_id`的更新通知时，系统将向您的Ping for Pull URL发送Pull请求。

>[!NOTE]
>
>403/Not Authorized for response your Ping（响应Ping）指示Ping请求附加的`lftoken`无效。 请确保`lftoken`适用于具有网络所有者权限的`user_id`或系统用户。 如果您使用Livefyre库，请使用`buildLivefyreToken`方法为请求生成有效的系统令牌。

1. 在您的页面中添加在用户更新其用户档案时ping Livefyre的代码。 通过以下方式构建URL:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** 您的Livefyre提供的网络名称。
   * **[!UICONTROL user_id:]** 您的用户ID。
   * **[!UICONTROL token:]** 有效的系统令牌。

1. 拉出请求结构。
