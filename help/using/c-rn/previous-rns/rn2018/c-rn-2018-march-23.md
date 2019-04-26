---
description: 2018年月23日发行说明。
seo-description: 2018年月23日发行说明。
seo-title: 2018 年 3 月 23 日
solution: Experience Manager
title: 2018 年 3 月 23 日
uuid: b69b8715-ace4-48e0-8f54-ce4 e12170 ef3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 2018 年 3 月 23 日{#march}

2018年月23日发行说明。

## 新增功能 {#section_syx_mdt_wcb}

此版本的生产版本中新增了以下功能：

* **生产中的新增功能：** Facebook创建了Facebook登录安全更新，这会导致客户的Facebook登录无法正常工作。要解决此问题，您必须：

   1. 在Client OAuth设置中添加以下URL到 **[!UICONTROL Valid OAuth redirect URIs]** 字段。替换 `<networkname>` 为正确的网络名称：
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. 切换 **[!UICONTROL Use Strict Mode for Redirect URI]****[!UICONTROL Yes]**到。

* **UAT中的新增功能：** 您现在可以在流中选择智能标签的置信阈值。为标签设置精度得分(0-100)可让您控制检索到的资产的准确性。

## 期刊 {#section_ehw_ndt_wcb}

此版本中解决了以下表中的问题。

## Production Release

| **期刊类型** | **组件** | **发行说明** |
|---|---|---|
| Bug | 媒体墙 | 修复了媒体墙中的一个问题，该问题导致在从流规则添加Instagram帖子时标记不可单击。 |
| Bug | Modq | 修复了ModQ未正确加载的问题。 |
| Bug | Modq | 修复了嵌入音频导致Modq停止工作的问题。 |

## UAT版本

| **期刊类型** | **组件** | **发行说明** |
|---|---|---|
| 增强功能 | 幻灯片 | 修复了一些问题，以使幻灯片更易于访问。 |
| 增强功能 | Studio | 您现在可以使用IMS登录登录Livefyre。 |

