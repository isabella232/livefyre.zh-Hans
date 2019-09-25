---
description: 使用Livefyre的社交用户管理系统。
seo-description: 使用Livefyre的社交用户管理系统。
seo-title: Livefyre Identity
solution: Experience Manager
title: Livefyre Identity
uuid: 5e9219b4-fbd7-40c6-9d57-129bb0649714
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# 使用Livefyre Identity{#livefyre-identity}

如果您使用自定义或第三方用户管理系统，请跳过此部分。

用户可以使用他们的社交媒体帐户或专门为您的网站创建的基于电子邮件的帐户登录您的应用程序。

Livefyre Identity包中包含委派身份验证所必需的信息。 （因此，Livefyre标识不需要显式身份验证委托。）

要将社交登录添加到Livefyre集成，请执行以下操作：

1. 创建社交应用程序。
1. 将您的应用程序连接到Livefyre。
1. 将Livefyre.js添加到页面。
1. 初始化Livefyre标识。

>[!NOTE]
>
>本文档列出了社交提供商应用程序创建流程的Livefyre特定方面。 Livefyre不负责对其界面进行任何更改，Livefyre也无法为创建这些应用程序或其批准过程提供帮助。 请使用可用的Twitter、Facebook、Yahoo！和Google开发人员信息创建这些应用程序，并导航其批准过程（如有必要）。

