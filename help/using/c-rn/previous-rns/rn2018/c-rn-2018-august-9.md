---
description: 2018年8月9日版本的发行说明。
seo-description: 2018年8月9日版本的发行说明。
seo-title: 2018 年 8 月 9 日
solution: Experience Manager
title: 2018 年 8 月 9 日
uuid: c59ae5ec-9d26-41c4-9a98-cb95c89ee26a
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 2018 年 8 月 9 日{#august}

2018年8月9日版本的发行说明。

## 新增功能 {#section_syx_mdt_wcb}

**** 视频智能标记：用户现在可以看到50MB以下视频的智能标记。

## 问题 {#section_ehw_ndt_wcb}

此版本中解决了下表中的问题。

## 生产版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 错误 | 应用程序内容 | 修复了管理员和内容管理者无法编辑应用程序内容中内容的问题。 |
| 增强功能 | 应用程序 | 社交网络已做出隐私更改，这意味着Facebook或Twitter不再支持社交提及。 |
| 增强功能 | 应用程序 | 社交网络已经对隐私做了更改。 “发布到”功能已被删除，该功能会自动将内容发布到社交网络(Facebook、LinkedIn、Twitter)。 |
| 增强功能 | GDPR | 从“设置”&gt;“隐私”下的请求详细信息页面删除了详细信息模式的切换。 在URL末尾添加/dbg仍可以访问详细信息模式切换。 |
| 错误 | 集成：AEM | 修复了在AEM中拖放Livefyre应用程序似乎会创建多个应用程序的问题。 |
| 错误 | 库 | 修复了资源未在库中正确保存的问题。 |
| 错误 | Livefyre Identity | 修复了LF标识在登录时导致403错误的问题。 |
| 错误 | 社交搜索 | 修复了用户无法使用社交搜索中的URL选项搜索公共Facebook帖子的问题。 |
| 增强功能 | 社交同步 | 社交网络已做出隐私更改，这意味着Facebook不再支持社交同步。 |
| 增强功能 | 流 | 现在，在删除应用程序时，您会删除与该应用程序关联的所有流。 |
| 增强功能 | Studio | Customers now have the ability to emit Livefyre events to Adobe Analytics individually as opposed to in batches. |
| 增强功能 | Studio | Modal windows that display in conversation Apps for social networks will now be modal windows from the social network instead of Adobe Experience Manager Livefyre or other branded modal windows. |

## UAT版本

The issues in the following tables were resolved in the UAT version release.

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 错误 | GDPR | 修复了某些Instagram视频不显示退出消息的问题。 |
| 错误 | 库 | 修复了授予权限的卡手动显示错误权限请求状态的问题。 |
| 错误 | 库 | 修复了无法将资产保存到文件夹的问题。 |
| 错误 | 库／搜索 | 恢复了在“社交搜索”中从Instagram搜索URL的功能。 |
| 错误 | ModQ | 修复了ModQ中的“更多信息”菜单未在预期位置显示的问题。 |
| 错误 | 权限管理 | 修复了页面滚动时ModQ中的排序应处于固定位置的问题。 |
| 错误 | 流 | 修复了在分阶段环境中查看流的问题。 |
| 增强功能 | 流 | 添加了“工作安全”(SFW)和“工作安全”(NSFW)切换到“流”。 |
| 增强功能 | Studio | 为通过FileStack上传到Livefyre Studio库的内容（“所有资产”中的上传功能）添加了智能标记功能。 |

