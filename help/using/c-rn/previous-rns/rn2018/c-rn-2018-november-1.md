---
description: 2018年11月日发行说明。
seo-description: 2018年11月日发行说明。
seo-title: 2018年11月日
solution: Experience Manager
title: 2018年11月日
uuid: ed1a3bf1-b3 f1-4746-8422-072823ba62
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 2018年11月日{#november}

2018年11月日发行说明。

## 新增功能 {#section_syx_mdt_wcb}

此版本的生产版本中发布了以下新增功能：

* 视频智能标签

   利用由Adobe Sensei支持的艺术计算机愿景技术的状态，在将视频内容保存到库时自动标记视频内容。智能标签可帮助您更有效地管理UGC，但还可以创建超精确的策展规则(流)，这些规则(流)根据视频中的内容而不是只能为文本收集内容，从而节省了您的大量工作。

   功能详细信息：

   * 智能标签会自动添加到从库中的社交搜索、流和上传的视频文件中获得的视频。查看单个视频的资产详细信息中的标记
   * 以MP4、. MOV和AVI格式标记视频
   * 标记60秒或50MB的视频
   * 视频的两种智能标签类别适用于视频：功能(动物、对象、地点等)和动作(运行、行走、唱歌等)
   有关更多信息，请参阅 [智能标签](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Instagram速率限制

   Instagram改变了使用Instagram API(包括Livefyre)的任何公司可以从每个令牌的5000次请求到每个令牌请求一小时的请求数。这称为 *速率限制*。有关更多信息，请参阅 [Instagram速率限制](/help/using/c-streams/c-instagram-rate-limiting.md)。

* 库中的音频文件

   您现在可以从库面板对音频文件执行以下功能：

   * 搜索
   * Preview
   * Import
   * 按音频文件过滤
   * 将文件拖放到设计人员中

## 期刊 {#section_ehw_ndt_wcb}

此版本的生产版本中未解决新问题。请参见 [上面](#c_rn/section_syx_mdt_wcb)的部分。

## UAT版本 {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

此版本的UAT版本中解决了以下表中的问题。

| **期刊类型** | **组件** | **发行说明** |
|---|---|---|
| 增强功能 | GDPR | 将删除Analytics中之前客户的所有数据。 |
| Bug | 库 | 修复了一个问题，该问题导致上传到库的视频，然后在资产详细信息中查看无法正确显示。 |
| Bug | Mosaic | 修复了一个问题，该问题导致Mosaic将Instagram轮盘中的最后一条内容显示为缩略图而不是卡。 |
| Bug | 社交搜索 | 修复了Instagram社交搜索无法正常工作的问题。 |

