---
description: 2018年2月15日版本的发行说明。
title: 2018 年 2 月 15 日
exl-id: 7276de37-c8cd-4e85-bc92-90c272e5bf94
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 5%

---

# 2018年2月15日{#february}

2018年2月15日版本的发行说明。

## 新增功能 {#section_syx_mdt_wcb}

以下功能是此版本的生产版本中的新增功能：

* **智能标签。**

   Livefyre使用Adobe Sensei图像识别技术自动为您保存在库中的图像添加标签。
使用智能标签，您可以节省大量搜索和管理内容的时间。 使用智能标记，您可以：

   * 根据图像内容（而非仅文本）搜索保存的图像以获得精确的内容
   * 根据用于分析图像（而非仅文本）的精确搜索词在流中收集内容

   有关智能标签的详细信息，请参阅[智能标签](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)。

* **产品内消息。** 现在，当您登录到Livefyre Studio时，会弹出一个公告窗口，显示有关新功能的更新。
* **传送的UGC。** 您现在可以在Livefyre Carousel应用程序中使用UGC Commerce的所有功能。您可以创建行动动员按钮，并将产品目录连接到应用程序以从传送创建购物体验。

## 问题 {#section_ehw_ndt_wcb}

此版本中解决了下表中的问题。

## 生产版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 问题 | ModQ | 修复了标记为已批准或已丢弃的Instagram帖子重新进入队列的问题。 |
| 增强功能 | Rights Management | 添加了一个增强功能，以在发出权限请求时尝试使用过期的Instagram帐户时显示警告。 |
| 问题 | 趋势 | 修复了趋势应用程序有时仍允许HTTP（而非HTTPS）的问题。 |

## UAT版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 增强功能 | 应用程序 | 添加了从Livefyre删除应用程序的功能。 |
| 问题 | 投票 | 更改了“投票”以只使用HTTPS。 以前，仍允许将投票与HTTP一起使用。 |
| 问题 | UGC | 修复了可视化应用程序中的UGC未按产品ID按预期过滤的问题。 |
