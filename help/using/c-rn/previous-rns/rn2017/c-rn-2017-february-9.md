---
description: 2017年2月9日版本的发行说明。
seo-description: 2017年2月9日版本的发行说明。
seo-title: 2017 年 2 月 9 日
title: 2017 年 2 月 9 日
uuid: cbbf10f3-d8ca-4c10-849e-fa7208f987be
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 5%

---


# 2017 年 2 月 9 日{#february}

2017年2月9日版本的发行说明。

## Twitter的SocialSync {#section_nv4_yry_wy}

SocialSync for Twitter多年来一直是我们核心功能的一部分。 但是，随着我们的产品的不断开发和发展，SocialSync for Twitter已成为一种低价值功能，目前我们一小部分客户都使用它。 为了改善Livefyre的客户整体体验，并将开发资源集中在最有价值的领域，我们将于2月24日停止SocialSync for Twitter功能。 此更新将不影响Facebook的SocialSync。 如果您对此更新有任何疑问或疑虑，请联系您的Livefyre CSM。

## 生产版本{#section_r24_1m2_wy}

| 问题类型 | 组件 | 发行说明 |
|--- |--- |--- |
| 错误 | 媒体墙 | 修复了允许Facebook视频正确播放的错误。 |
| 错误 | ModQ | 修复了阻止电子邮件主题不显示在电子邮件流内容中的错误。 |
| 错误 | 马赛克 | 为Mosaic添加了其他辅助功能支持，允许用户在内容卡之间切换选项卡。 |
| 错误 | 评论 | 修复了导致评级编辑无法正确显示的错误。 |
| 错误 | 社交搜索 | 修复了导致Twitter列表搜索结果中“显示更多”按钮被切断的错误。 |
| 增强功能 | Storify 2 | 增强的Storify 2支持文案免费内容搜索。 Flickr、名词项目、Kuler、Pixabay和Unsplash中的文案免费搜索免费图像。 |
| 错误 | 流 | 修复了阻止保存Tumblr流规则的错误。 |
| 错误 | 流 | 修复了在RSS源的集合JSON中生成错误生成器ID的错误。 |
| 增强功能 | 流 | 对默认禁用的“仅验证帐户”选项的设置进行了调整。 |
| 增强功能 | 流 | 添加了允许列出和绕过仲裁的类别内容（通过流规则）的新功能。 |
| 错误 | 流 | 修复了导致“预审核”和“媒体预审核”设置转移到新创建的流规则的错误。 |

## UAT版本{#section_dyx_yl2_wy}

| 问题类型 | 组件 | 发行说明 |
|--- |--- |--- |
| 错误 | 对话应用程序 | 增强的对话应用程序，可始终与用户用户档案链接，即使没有完全的身份验证集成也是如此。 |
| 错误 | 马赛克 | 修复了现在通过HTTPS提供所有Twitter图像的错误。 |
| 错误 | 社交搜索 | 修复了在社交搜索中保存资产并在库中查看资产时，导致绿色“已保存”复选标记不显示的错误。 |
| 错误 | 社交搜索 | 修复了“隐藏显式图像”选项无法正常工作的错误。 |
| 增强功能 | Storify 2 | 增强的Storify 2支持打开模态的永久链接（以前，应用程序将滚动到页面上的帖子位置）。 在Storify 2的Designer中，我们添加了一种配置，以在“滚动”(Scroll)和“模态”(Modal)行为之间切换。 Modal Permalink行为将是默认行为。 |
| 增强功能 | Storify 2 | 增强了Storify 2 Google AMP集成，以生成较小的CSS文件。 |
| 错误 | 流 | 电子邮件流规则中的增强内容（图像和视频）可通过HTTPS提供。 |
| 错误 | 流 | 在Twitter流规则的映射中为“Mile Radius”值添加了标签。 |
| 错误 | 流 | 修复了Facebook和Facebook页面流规则的错误，可相应地拉入包含多个媒体附件的帖子。 |
| 错误 | Studio | 修复了在Studio中使用过滤器时导致多个&amp;被附加到URL的错误。 |
| 错误 | Studio | 修复了阻止Studio过滤器中某些复选框允许取消选中的错误。 |

