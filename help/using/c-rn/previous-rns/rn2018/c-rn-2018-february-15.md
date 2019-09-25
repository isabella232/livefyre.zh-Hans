---
description: 2018年2月15日版本的发行说明。
seo-description: 2018年2月15日版本的发行说明。
seo-title: 2018 年 2 月 15 日
solution: Experience Manager
title: 2018 年 2 月 15 日
uuid: ee46f088-9fb7-49e2-a42c-e0d4b2f24a32
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# February 15, 2018{#february}

2018年2月15日版本的发行说明。

## 新增功能 {#section_syx_mdt_wcb}

以下功能是此版本生产版本中的新增功能：

* **智能标记。**

   Livefyre使用Adobe Sensei图像识别技术自动标记您保存在库中的图像。
使用智能标记，您可以节省大量搜索和审核内容的时间。 使用智能标记，您可以：

   * 根据图像内容（而非仅文本）搜索保存的图像以获得精确的内容
   * 根据用于分析图像的精确搜索词（而非仅文本）在流中收集内容
   有关智能标记的详细信息，请参阅 [智能标记](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)。

* **产品内消息。** 现在，当您登录到Livefyre studio时，会弹出一个公告窗口，显示有关新功能的更新。
* **传送的UGC。** 您现在可以在Livefyre Carousel应用程序中使用UGC Commerce的所有功能。 您可以创建“行动动员按钮”，并将产品目录连接到应用程序以从传送创建购物体验。

## 问题 {#section_ehw_ndt_wcb}

此版本中解决了下表中的问题。

## 生产版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 问题 | ModQ | 修复了标记为已批准或已破坏的Instagram帖子重新进入队列的问题。 |
| 增强功能 | 权限管理 | 添加了增强功能，以在发出权限请求时尝试使用过期的Instagram帐户时显示警告。 |
| 问题 | 趋势 | 修复了Trends应用程序有时仍允许HTTP而不是HTTPS的问题。 |

## UAT版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 增强功能 | 应用程序 | 添加了从Livefyre删除应用程序的功能。 |
| 问题 | 投票 | 将“投票”更改为只使用HTTPS。 以前，投票仍允许与HTTP一起使用。 |
| 问题 | UGC | 修复了可视化应用程序中的UGC未按预期的产品ID过滤的问题。 |

