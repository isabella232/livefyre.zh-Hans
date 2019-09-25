---
description: 2018年3月23日版本的发行说明。
seo-description: 2018年3月23日版本的发行说明。
seo-title: 2018 年 3 月 23 日
solution: Experience Manager
title: 2018 年 3 月 23 日
uuid: b69b8715-ace4-48e0-8f54-ce4e12170ef3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# March 23, 2018{#march}

2018年3月23日版本的发行说明。

## 新增功能 {#section_syx_mdt_wcb}

以下功能是此版本生产版本中的新增功能：

* **** 生产方面的新增功能：Facebook创建了对Facebook登录的安全更新，该更新将导致客户的Facebook登录无法正确工作。 要解决此问题，您必须：

   1. 将以下URL添加到“Client OAuth **[!UICONTROL Valid OAuth redirect URIs]** Settings”中的字段。 用您 `<networkname>` 的正确网络名称替换：
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. 切换 **[!UICONTROL Use Strict Mode for Redirect URI]** 到 **[!UICONTROL Yes]**。

* **** UAT的新增功能：您现在可以为流中的智能标签选择置信度阈值。 为标记设置精确度得分(0-100)可让您控制我们正在检索的资产的准确性。

## 问题 {#section_ehw_ndt_wcb}

此版本中解决了下表中的问题。

## 生产版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 错误 | 媒体墙 | 修复了媒体墙中的一个问题，该问题导致从流规则添加Instagram帖子时，标记无法单击。 |
| 错误 | ModQ | 修复了ModQ无法正确加载的问题。 |
| 错误 | ModQ | 修复了嵌入音频导致ModQ停止工作的问题。 |

## UAT版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 增强功能 | 幻灯片 | 修复了一些问题，使幻灯片更易于访问。 |
| 增强功能 | Studio | 您现在可以使用IMS登录名登录Livefyre。 |

