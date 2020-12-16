---
description: 2018年11月1日版本的发行说明。
seo-description: 2018年11月1日版本的发行说明。
seo-title: 2018 年 11 月 1 日
solution: Experience Manager
title: 2018 年 11 月 1 日
uuid: ed1a3bf1-b3f1-4746-8462-07283723ba62
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 5%

---


# 2018 年 11 月 1 日{#november}

2018年11月1日版本的发行说明。

## 新增功能 {#section_syx_mdt_wcb}

此版本的生产版本中发布了以下新功能：

* 视频智能标记

   利用由Adobe Sensei提供支持的最新计算机视觉技术，在将视频内容保存到库时自动标记视频内容。 智能标记可以帮助您更有效地管理UGC，同时创建超精确的特选规则（流），这些规则根据视频中的内容（而不仅仅是文本）收集内容，从而节省您协调多余内容的大量工作。

   功能详细信息：

   * 智能标记会自动添加到从库中的社交搜索、流和上传的视频文件获取的视频中。 视图在单个视频的资产详细信息中标记
   * 以。MP4、.MOV和AVI格式标记视频
   * 为视频标记高达60秒或50MB
   * 两类别智能标记应用于视频：特征（动物、物体、地点等）和动作（跑步、行走、唱歌等）

   有关详细信息，请参阅[智能标记](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Instagram速率限制

   Instagram已更改了任何使用Instagram API的公司（包括Livefyre）可以发出的请求数，从每个令牌每小时5,000个请求到每个令牌每小时200个请求。 这称为&#x200B;*速率限制*。 有关详细信息，请参阅[Instagram速率限制](/help/using/c-streams/c-instagram-rate-limiting.md)。

* 库中的音频文件

   您现在可以从库面板对音频文件执行以下功能：

   * 搜索
   * 预览
   * 导入
   * 按音频文件过滤
   * 将文件拖放到设计人员中

## 问题 {#section_ehw_ndt_wcb}

此版本的生产版本中未解决任何新问题。 请参阅上面的[部分](#c_rn/section_syx_mdt_wcb)。

## UAT版本{#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

以下表中的问题已在此版本的UAT版本中解决。

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 增强功能 | GDPR | 将删除Analytics中归属于前客户的所有数据。 |
| 错误 | 库 | 修复了上传到库，然后在资产详细信息中查看的视频无法正确显示的问题。 |
| 错误 | 马赛克 | 修复了Mosaic将Instagram传送的最后一段内容显示为缩略图而非卡的问题。 |
| 错误 | 社交搜索 | 修复了Instagram社交搜索未按预期工作的问题。 |

