---
description: 2017年6月1日版本的发行说明。
title: 2017 年 6 月 1 日
exl-id: 82e02d9f-97d7-4f80-8382-9ccf7ac3dcf5
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 6%

---

# 2017 年 6 月 1 日{#june}

2017年6月1日版本的发行说明。

## 生产版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 增强功能 | 应用程序内容 | 添加了一项增强功能，允许应用程序内容中的用户下载已上传到Livefyre应用程序和/或通过上传媒体API的本机视频文件。 |
| 错误 | 马赛克 | 修复了Mosaic中阻止在页面刷新后加载新创建的Mosaic的错误。 |
| 错误 | Rights Management | 修复了导致Rights Management中断处理新删除的/标记为私有的Instagram和Twitter内容的错误。 |
| 错误 | Storify 2 | 更新了Storify 2中的排序标签以匹配预期行为。 “最旧到最新”和“最新到最旧”现在将说“从头到尾”和“从头到尾”。 排序顺序基于Storify 2的编辑器中规定的顺序，而不是发布日期。 |

## UAT版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 错误 | 评论 | 修复了“审阅”中的一个错误，以确保所有实施中通过HTTPS加载媒体。 |
| 错误 | 搜索 | 修复了导致Instagram位置搜索结果显示重复的错误。 |
| 错误 | Siestr | 增强的侧滑以支持前端协调。 这意味着登录到前端应用程序的版主将能够批准或删除内容。 |
| 错误 | 流规则 | 为Twitter流添加了增强功能，以便所有映射位置都列在规则摘要中 |
| 错误 | 流规则 | 修复了允许Twitter流用户同时存在于“is posted by any these authors”和“is not posted by any these authors”字段中的错误。 |
| 增强功能 | 流规则 | 添加了在流规则中按语言过滤帖子的功能 |
