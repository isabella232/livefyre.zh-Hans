---
description: 使用“为拉取进行ping”可保持Livefyre与用户管理系统同步。
seo-description: 使用“为拉取进行ping”可保持Livefyre与用户管理系统同步。
seo-title: 与Livefyre同步使用Ting for Draw
solution: Experience Manager
title: 与Livefyre同步使用Ting for Draw
uuid: 7b059064-1ca-46d7-8055-dfe59 f493 ac1
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 与Livefyre同步使用Ting for Draw{#sync-with-livefyre-using-ping-for-pull}

使用“为拉取进行ping”可保持Livefyre与用户管理系统同步。

通常， ***在您的网站/应用程序的用户(显示姓名、头像等)中，您可以随时ping*** Livefyre(显示姓名、头像等)，以及Livefyre ***提取*** 该用户的更新配置文件。

![](assets/Ping-for-Pull.png)

获取序列的ping：

1. 客户向Livefyre发送ping请求(包括要更新的用户)。
1. Livefyre确认收到了HTTP200/成功消息。
1. Livefyre处理拉动请求。
1. Livefyre队列提取请求。
1. Livefyre执行将请求拖动到端点以捕获更新的用户信息。
1. 客户收到提取响应和验证。
1. Livefyre使用拖曳端点中包含的外部配置文件信息更新远程配置文件。

每当用户更新其配置文件信息时，都可以使用Ting Livefyre。虽然根据网络负载进行ping完成的时间可能因网络负载而异，但它将在到10分钟之间更新用户信息。更新的配置文件更改将首先显示在Livefyre Studio>用户中。

更新的配置文件信息将在两次活动后显示在Livefyre Apps中：

* 用户注销，然后登录应用程序。在UserAuthToken中显示名称值优先于“在推送中提取”更新。用户注销/登录将刷新令牌以更新会话。

   要在更新配置文件信息时生成新的UserTokens，请使用SSO authDelegate将用户注销，然后在后台再次登录。

* 对集合进行bootstrap更新将显示更新的信息(最多每5-10分钟)。

要为用户配置文件系统实施ping，请执行以下操作：

1. [构建拖动端点](#t_build_the_pull_endpoint)。

   >[!NOTE]
   >
   >Livefyre库包含一个SyncUser方法，用于使用户配置文件保持最新状态。如果您使用Livefyre库，请跳过接下来的两个步骤。

1. [在Studio](#register_the_endpoint_with_studio)中注册拖动端点。
1. [构建Ping](#t_build_the_ping)。
1. [构建用于拉动响应]的ping。(# reference_ n3 x_ pzb_ mz)
