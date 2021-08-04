---
description: 2018年11月15日版本的发行说明。
title: 发行说明
exl-id: 3f904022-b770-4f35-a3b0-790e15748763
source-git-commit: beb224fdccf68c98fc3eff62b0867f22fa52902b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 6%

---

# 发行说明{#release-notes}

2018年11月15日版本的发行说明。

## 新增功能 {#section_syx_mdt_wcb}

此版本的生产版本中发布了以下新功能：

* **更新了Instagram搜索和流。** 您可以使用Instagram *业务* 帐户：

   * 按用户执行Instagram社交搜索(用户也必须是Instagram商业帐户)。

   * 从特定的Instagram用户帐户（该帐户也必须是业务帐户）创建Instagram流，包括您自己的帐户。

   * 使用部分自动化的工作流从Instagram请求资产权限。

   * 有关需要设置哪种类型的Instagram帐户并从Instagram请求权限的信息，请参阅[关于Instagram帐户](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)。

* **自动监控使用权限请求响应的基于业务帐户的搜索。** 仅适用于基于业务帐户的搜索 — 能够自动监视对权限请求的响应并更新Livefyre中的活动历史记录。

有关如何请求Instagram帐户权限的更多信息，请参阅[手动发送Instagram权限请求](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md)和[发送部分自动化的Instagram权限请求](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)。

* **Adobe Target 集成.** 添加了与Adobe Target的集成，允许您将Livefyre应用程序直接共享到Adobe Target选件库。有关将Livefyre与Adobe Target结合使用的更多信息，请参阅[Target文档](https://experienceleague.adobe.com/docs/livefyre/using/library/livefyre-target.html)。

## 问题 {#section_ehw_ndt_wcb}

此版本解决了下表中的问题。

### 生产版本

| 问题类型 | 组件 | 发行说明 |
|--- |--- |--- |
| 问题 | AppService:Livefyre Identity | 修复了在Studio >集成设置> Livefyre Identity中单击[!UICONTROL Reset to Default]未将登录模式下的徽标重置为默认图像的问题。 |
| 问题 | 库 | 修复了上传到库后在资产详细信息中查看的视频无法正确显示的问题。 |
| 问题 | 流 | 修复了阻止产品在流规则中显示的问题。 |
| 问题 | 流 | 修复了产品标记不适用于流规则的问题。 |
| 增强功能 | Studio | 修复了Livefyre Studio中未显示产品ID的问题。 |
| 问题 | 工作室：ModQ | 修复了删除后，已删除的内容仍显示在ModQ中的问题。 |

### UAT版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 问题 | 社交组件：轮播 | 修复了共享链接未响应并复制IE11和Mozilla Firefox中预期的URL的问题。 |
