---
description: 2018年11月1日版本的发行说明。
title: 2018 年 11 月 1 日
exl-id: b12b6a56-f14f-4447-9fde-25cb3acf6665
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 4%

---

# 2018 年 11 月 1 日{#november}

2018年11月1日版本的发行说明。

## 新增功能 {#section_syx_mdt_wcb}

此版本的生产版本中发布了以下新功能：

* 视频智能标签

   利用由Adobe Sensei提供支持的最新计算机视觉技术，在将视频内容保存到库时自动标记视频内容。 “智能标签”可帮助您更有效地管理UGC，还可创建超精确的特选规则（流），这些规则（流）可根据视频中的内容收集内容，而不仅仅是文本，从而为您节省管理多余内容的大量精力。

   功能详细信息：

   * 智能标记会自动添加到通过社交搜索、流和库中上传的视频文件获取的视频中。 视图在单个视频的资产详细信息中标记
   * 以.MP4、.MOV和AVI格式为视频添加标签
   * 为视频添加最多60秒或50MB的标记
   * 两类别智能标签适用于视频：（动物、物体、地点等）和动作（跑步、行走、唱歌等）

   有关详细信息，请参阅[智能标签](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Instagram速率限制

   Instagram已将使用Instagram API（包括Livefyre）的任何公司可以发出的请求数从每小时每个令牌5,000个请求更改为每小时每个令牌200个请求。 这称为&#x200B;*速率限制*。 有关详细信息，请参阅[Instagram速率限制](/help/using/c-streams/c-instagram-rate-limiting.md)。

* 库中的音频文件

   您现在可以从“库”面板对音频文件执行以下功能：

   * 搜索
   * 预览
   * 导入
   * 按音频文件过滤
   * 将文件拖放到设计器中

## 问题 {#section_ehw_ndt_wcb}

此版本的生产版本中未解决任何新问题。 请参阅上面的[部分。](#c_rn/section_syx_mdt_wcb)

## UAT版本{#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

以下表中的问题已在此版本的UAT版本中解决。

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 增强功能 | GDPR | 将删除Analytics中归属于前客户的所有数据。 |
| 错误 | 库 | 修复了上传到库，然后在资源详细信息中查看的视频未正确显示的问题。 |
| 错误 | 马赛克 | 修复了Mosaic将Instagram轮盘中的最后一段内容显示为缩略图（而非卡）的问题。 |
| 错误 | 社交搜索 | 修复了Instagram社交搜索未按预期工作的问题。 |
