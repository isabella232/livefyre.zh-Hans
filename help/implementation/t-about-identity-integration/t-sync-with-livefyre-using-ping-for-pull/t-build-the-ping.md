---
description: 生成ping命令，以便在用户更新其用户档案时，您的页面ping Livefyre。
title: 构建Ping
exl-id: 626c200b-eaff-483f-b1eb-7d8993fe5e7c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# 生成Ping{#build-the-ping}

生成ping命令，以便在用户更新其用户档案时，您的页面ping Livefyre。

当Livefyre收到`networkName`和`user_id`的更新通知时，系统将向您的Ping for Pull URL发送Pull请求。

>[!NOTE]
>
>403/Not Authorized for your Ping指示Ping请求后附加的`lftoken`无效。 请确保`lftoken`适用于具有网络所有者权限的`user_id`或系统用户。 如果您使用的是Livefyre库，请使用`buildLivefyreToken`方法为请求生成有效的系统令牌。

1. 在您的页面中添加在用户更新其用户档案时ping Livefyre的代码。 通过以下方式构建URL:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** 您的Livefyre提供的网络名称。
   * **[!UICONTROL user_id:]** 您的用户ID。
   * **[!UICONTROL token:]** 有效的系统令牌。

1. 拉出请求结构。
