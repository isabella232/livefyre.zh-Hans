---
description: 使用Ping for Pull可使Livefyre与您的用户管理系统保持同步。
seo-description: 使用Ping for Pull可使Livefyre与您的用户管理系统保持同步。
seo-title: 使用Ping for Pull与Livefyre同步
solution: Experience Manager
title: 使用Ping for Pull与Livefyre同步
uuid: 7b059064-1cca-46d7-8055-dfe59f493ac1
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# 使用Ping for Pull与Livefyre同步{#sync-with-livefyre-using-ping-for-pull}

使用Ping for Pull可使Livefyre与您的用户管理系统保持同步。

通常，每当您的网站／应用程序用户更新其配置文件（显示名称、头像等）时，您都会Ping ***Livefyre，然后Livefyre********* 拉取该用户的更新配置文件。

![](assets/Ping-for-Pull.png)

Ping for Pull Sequence:

1. 客户向Livefyre发送Ping请求（包括要更新的用户）。
1. Livefyre确认接收到Ping（HTTP 200/成功）。
1. Livefyre处理拉取请求。
1. Livefyre队列拉取请求。
1. Livefyre对端点执行拉取请求以捕获更新的用户信息。
1. 客户收到拉取响应并验证。
1. Livefyre使用“拉取”端点中包含的外部配置文件信息更新远程配置文件。

每当用户更新其个人资料信息时，Ping Livefyre。 尽管Ping for Pull完成时间可能因网络负载而异，但它将在1到10分钟内更新用户信息。 更新的配置文件更改将首先在Livefyre Studio &gt;用户中显示。

在发生以下两个事件后，更新的配置文件信息将显示在Livefyre应用程序中：

* 用户注销，然后重新登录到应用程序。 用户身份验证令牌中的显示名称值优先于Ping以获取更新。 用户注销／登录将刷新令牌以更新会话。

   要在更新配置文件信息时生成新的userAuthTokens，请使用SSO authDelegate在后台将用户注销，然后再次登录。

* 对集合进行引导更新将导入更新的信息（最多每5-10分钟）。

要为用户配置文件系统实施Ping for Pull，请执行以下操作：

1. [构建拉取端点](#t_build_the_pull_endpoint)。

   >[!NOTE]
   >
   >Livefyre库包含同步用户方法，可让用户配置文件保持最新。 如果您使用Livefyre库，请跳过接下来的两个步骤。

1. [在Studio中注册拉取端点](#register_the_endpoint_with_studio)。
1. [构建Ping](#t_build_the_ping)。
1. [构建Ping以获取响应]。(#reference_n3x_pzb_mz)
