---
description: 2017年2月9日版本的发行说明。
title: 2017 年 2 月 9 日
exl-id: 155f8a43-17e5-40b2-ada0-32691f8a34e5
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 5%

---

# 2017 年 2 月 9 日{#february}

2017年2月9日版本的发行说明。

## twitter {#section_nv4_yry_wy}的SocialSync

twitter的SocialSync是我们核心功能的一部分已有数年。 但是，随着我们的产品不断开发和发展，Twitter的SocialSync已成为一项低价值功能，目前只有一小部分客户使用它。 为了改善Livefyre的整体客户体验，并将开发资源集中在价值最高的领域，我们将于2月24日停止Twitter的SocialSync功能。 此更新将不影响Facebook的SocialSync。 如果您对此更新有任何疑问或疑虑，请联系您的Livefyre CSM。

## 生产版本{#section_r24_1m2_wy}

| 问题类型 | 组件 | 发行说明 |
|--- |--- |--- |
| 错误 | 媒体墙 | 修复了允许Facebook视频正确播放的错误。 |
| 错误 | ModQ | 修复了阻止电子邮件主题不显示在电子邮件流内容中的错误。 |
| 错误 | 马赛克 | 增加了对Mosaic的附加辅助功能支持，允许用户在内容卡之间切换选项卡。 |
| 错误 | 评论 | 修复了阻止评级编辑正确显示的错误。 |
| 错误 | 社交搜索 | 修复了导致Twitter列表搜索结果中“显示更多”按钮被切断的错误。 |
| 增强功能 | Storify 2 | 增强的Storify 2支持“文案免费”内容搜索。 文案免费搜索Flickr、Noun Project、Kuler、Pixabay和Unsplash中的免费文案图像。 |
| 错误 | 流 | 修复了阻止Tumblr流规则保存的错误。 |
| 错误 | 流 | 修复了在RSS源的Collection JSON中生成错误生成器ID的错误。 |
| 增强功能 | 流 | 对默认禁用的“仅验证帐户”选项的设置进行了调整。 |
| 增强功能 | 流 | 添加了允许列出和绕过审核的类别内容（通过流规则）的新功能。 |
| 错误 | 流 | 修复了导致“预审”和“媒体预审”设置转换到新创建的流规则的错误。 |

## UAT版本{#section_dyx_yl2_wy}

| 问题类型 | 组件 | 发行说明 |
|--- |--- |--- |
| 错误 | 对话应用程序 | 增强的对话应用程序，可始终链接到用户用户档案，即使没有完全身份验证集成也是如此。 |
| 错误 | 马赛克 | 修复了现在通过HTTPS提供所有Twitter图像的错误。 |
| 错误 | 社交搜索 | 修复了在Social Search中保存资源并查看库中的资源时，导致绿色“已保存”复选标记不显示的错误。 |
| 错误 | 社交搜索 | 修复了“隐藏显式图像”选项无法正常工作的错误。 |
| 增强功能 | Storify 2 | 增强的Storify 2支持打开模式的超链接（以前，应用程序将滚动到页面上的帖子位置）。 在Storify 2的Designer中，我们添加了一个配置，用于在“滚动”(Scroll)和“模态”(Modal)行为之间切换。 Modal Permalink行为将是默认行为。 |
| 增强功能 | Storify 2 | 增强了Storify 2 Google AMP集成以生成更小的CSS文件。 |
| 错误 | 流 | 电子邮件流规则中的增强内容（图像和视频）可通过HTTPS提供。 |
| 错误 | 流 | 在Twitter流规则中的映射中为“Mile Radius”值添加了标签。 |
| 错误 | 流 | 修复了Facebook和Facebook页面蒸汽规则的错误，可以相应地拉入包含多个媒体附件的帖子。 |
| 错误 | Studio | 修复了在Studio中使用过滤器时导致多个&amp;附加到URL的错误。 |
| 错误 | Studio | 修复了阻止Studio过滤器中的某些复选框允许取消选中的错误。 |
