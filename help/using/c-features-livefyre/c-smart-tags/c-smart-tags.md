---
description: 'null'
seo-description: 'null'
seo-title: 智能标记
title: 智能标记
uuid: f978fa83-e79b-46ae-bb3e-0f9449bd0440
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# 智能标记{#smart-tags}

Livefyre使用Adobe Sensei计算机视觉技术自动标记您在库中保存或上传的图像和视频。

使用智能标记，您可以节省大量时间、管理、搜索和管理内容。 使用智能标记，您可以：

* 根据图像和视频内容（而非仅文本）搜索保存和上传的图像和视频，以获得精确的内容
* 根据用于分析图像或视频的精确搜索词（而非仅文本）在流中收集内容

当您保存或上传图像或视频时，Adobe Sensei会自动审阅内容并用135,000个分类器标记它，分三个类别:

* 特征（例如，猫、狗、金字塔、地标）
* 类别（例如，旅游、旅游、美容）
* 审美属性（例如，画质，第三种规则）
* SFW/NSFW(这允许您自动过滤NSFW图像，从而提高流和UGC库的安全性

智能标签排名算法使用智能标签置信度得分过滤器内容，内容有多新，以及用户为内容分配的星数。

**视频的智能标记**

功能详细信息：

* 智能标记应用于MP4、.avi和。mov视频格式
* 支持的视频的最大持续时间为60秒或50MB
* 智能标记在库中的社交搜索、流和已上传视频文件中可用

标记类型：

* 功能标签：功能与图像的功能标签（例如，猫、狗、金字塔、地标）相同。
* 操作标记：识别跨多个框架而非仅一个框架的功能。 这些功能在总结视频内容时更加有效。

有关智能标记的其他信息，请参阅[所有流规则的流规则选项](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
