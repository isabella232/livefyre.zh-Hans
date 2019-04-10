---
description: 2018年11月15日发行说明发行说明。
seo-description: 2018年11月15日发行说明发行说明。
seo-title: 发行说明
solution: Experience Manager
title: 发行说明
uuid: 34e64943-dea6-46ac-9cfc-8febeab6 aa42
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 发行说明{#release-notes}

2018年11月15日发行说明发行说明。

## 新增功能 {#section_syx_mdt_wcb}

此版本的生产版本中发布了以下新增功能：

* **Instagram搜索和流的更新。** 您可以使用 *Instagram业务帐户* 来：

   * 按用户执行Instagram社交搜索(用户必须是Instagram业务帐户)。

   * 从特定Instagram用户帐户(帐户也必须是业务帐户)创建Instagram流(包括您自己的帐户)。

   * 使用部分自动化工作流程，从Instagram请求资产权限。

   * 有关您需要设置和请求Instagram权限的Instagram帐户类型的信息，请 [参阅关于Instagram帐户](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)。

* **自动监控使用权限请求响应以进行基于业务帐户的搜索。** 仅针对基于业务帐户的搜索—可以自动监视对权限请求的答复并更新Livefyre中的活动历史记录。

有关如何请求Instagram帐户权限的详细信息，请参阅 [发送Instagram权限请求手动](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) 和 [发送部分自动化Instagram权限请求](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)。

* **Adobe Target集成。** 添加了与Adobe Target的集成，可让您直接将Livefyre应用程序共享到Adobe Target选件库。有关将Livefyre与Adobe Target结合使用的更多信息，请参阅 [Target文档](https://marketing.adobe.com/resources/help/en_US/livefyre/livefyre-target.html)。

## 期刊 {#section_ehw_ndt_wcb}

此版本中解决了以下表中的问题。

### Production Release

| 期刊类型 | 组件 | 发行说明 |
|--- |--- |--- |
| 期刊 | AppService：Livefyre Identity | 修复了单击该问题的问题 [！UICCONTROL重置为默认] 值未在“Studio”>“Integration Settings”>“Livefyre Identity”中的“登录模式”下重置徽标至默认图像。 |
| 期刊 | 库 | 修复了一个问题，该问题导致上传到库的视频，然后在资产详细信息中查看无法正确显示。 |
| 期刊 | 流媒体 | 修复了阻止产品在流规则中显示的问题。 |
| 期刊 | 流媒体 | 修复了产品标记不可用于流规则的问题。 |
| 增强功能 | Studio | 修复了未在Livefyre Studio中显示产品ID的问题。 |
| 期刊 | Studio：Modq | 修复了删除内容在ModQ删除后仍显示在ModQ中的问题。 |

### UAT版本

| **期刊类型** | **组件** | **发行说明** |
|---|---|---|
| 期刊 | 社交组件：Carousel | 修复了共享链接未响应并复制IE11和Mozilla Firefox中所需URL的问题。 |