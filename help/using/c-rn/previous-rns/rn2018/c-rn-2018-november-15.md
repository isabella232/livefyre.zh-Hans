---
description: 2018年11月15日版本的发行说明。
seo-description: 2018年11月15日版本的发行说明。
seo-title: 发行说明
solution: Experience Manager
title: 发行说明
uuid: 34e64943-dea6-46ac-9fcc-8febeab6aa42
translation-type: tm+mt
source-git-commit: efb031b58f01ec69c8297a808998d25a0015f102
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 7%

---


# 发行说明{#release-notes}

2018年11月15日版本的发行说明。

## 新增功能 {#section_syx_mdt_wcb}

此版本的生产版本中发布了以下新功能：

* **Instagram搜索和流的更新。** 您可以使用Instagram *商业帐户* :

   * 按用户进行Instagram社交搜索（用户也必须是Instagram商业帐户）。

   * 从特定Instagram用户帐户（该帐户也必须是商业帐户）创建Instagram流，包括您自己的帐户。

   * 使用部分自动化的工作流程从Instagram请求资产权限。

   * 有关您需要从Instagram设置和请求权限的Instagram帐户类型的信息，请参 [阅关于Instagram帐户](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)。

* **自动监控使用权限，为基于业务帐户的搜索请求响应。** 仅对于基于业务帐户的搜索——可以自动监视对权限请求的响应并更新Livefyre中的活动历史记录。

有关如何请求Instagram帐户权限的详细信息，请参 [阅手动发送Instagram权限请求](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md)[和发送部分自动化的Instagram权限请求](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)。

* **Adobe Target 集成.** 增加了与Adobe Target的集成，允许您直接将Livefyre应用程序共享到您的Adobe Target优惠库。 有关将Livefyre与Adobe Target结合使用的更多信息，请参阅 [目标文档](hhttps://docs.adobe.com/content/help/en/livefyre/using/library/livefyre-target.html)。

## 问题 {#section_ehw_ndt_wcb}

此版本中解决了下表中的问题。

### 生产版本

| 问题类型 | 组件 | 发行说明 |
|--- |--- |--- |
| 问题 | AppService:Livefyre Identity | 修复了在Studio > Integration Settings > Livefyre Identity中单 [!UICONTROL Reset to Default] 击未将“登录模式”下的徽标重置为默认图像的问题。 |
| 问题 | 库 | 修复了上传到库，然后在资产详细信息中查看的视频无法正确显示的问题。 |
| 问题 | 流 | 修复了阻止产品在流规则中显示的问题。 |
| 问题 | 流 | 修复了流规则中产品标记不可用的问题。 |
| 增强功能 | Studio | 修复了Livefyre Studio中未显示产品ID的问题。 |
| 问题 | Studio:ModQ | 修复了删除内容后，已删除内容仍显示在ModQ中的问题。 |

### UAT版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 问题 | 社交组件：旋转 | 修复了共享链接未响应并复制IE11和Mozilla Firefox中期望的URL的问题。 |