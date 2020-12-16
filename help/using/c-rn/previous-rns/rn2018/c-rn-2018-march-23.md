---
description: 2018年3月23日版本的发行说明。
seo-description: 2018年3月23日版本的发行说明。
seo-title: 2018 年 3 月 23 日
solution: Experience Manager
title: 2018 年 3 月 23 日
uuid: b69b8715-ace4-48e0-8f54-ce4e12170ef3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 7%

---


# 2018年3月23日{#march}

2018年3月23日版本的发行说明。

## 新增功能 {#section_syx_mdt_wcb}

以下是此版本的生产版本中的新增功能：

* **生产中的新** 增功能：Facebook创建了Facebook登录的安全更新，该更新将导致客户的Facebook登录无法正确工作。要解决此问题，您必须：

   1. 在“Client OAuth Settings（客户端OAuth设置）”中，将以下URL添加到&#x200B;**[!UICONTROL Valid OAuth redirect URIs]**&#x200B;字段。 将`<networkname>`替换为正确的网络名称：
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. 将&#x200B;**[!UICONTROL Use Strict Mode for Redirect URI]**&#x200B;切换为&#x200B;**[!UICONTROL Yes]**。

* **UAT中的新增功** 能：您现在可以为流中的智能标记选择置信阈值。通过设置标记的精确度得分(0-100)，您可以控制我们正在检索的资产的准确性。

## 问题 {#section_ehw_ndt_wcb}

此版本中解决了下表中的问题。

## 生产版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 错误 | 媒体墙 | 修复了媒体墙中从流规则添加Instagram帖子时无法点击标记的问题。 |
| 错误 | ModQ | 修复了ModQ无法加载的问题。 |
| 错误 | ModQ | 修复了嵌入音频导致ModQ停止工作的问题。 |

## UAT版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 增强功能 | 幻灯片 | 修复了一些问题，使幻灯片更易于访问。 |
| 增强功能 | Studio | 您现在可以使用IMS登录名登录Livefyre。 |

