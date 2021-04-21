---
description: 自定义Livefyre Siestr的文本字符串
title: 表示文本字符串
exl-id: 132a7c8d-10e1-419c-9d79-a40553e70785
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 13%

---

# 表示文本字符串{#sidenotes-text-strings}

自定义Livefyre Siestr的文本字符串

本页列表和描述了在Siserv应用程序中可自定义的所有字符串。 有关核心Livefyre应用程序可用字符串的信息，请参阅字符串自定义。

实施
身份验证
流信息
作者/内容信息
用户操作
帖子功能
审查方界面
错误

## 实施 {#section_wp2_ql4_xz}

要实现此功能，请传递要覆盖的字符串的1-1对象映射到Javascript配置对象。 如果您不提供字段，则将使用默认文本。

示例：

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" 
}; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## 身份验证{#section_pqf_3l4_xz}

可用于身份验证过程的字符串，以及已验证的用户菜单中的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 身份验证菜单字符串 | menuAuthSignInBtn | 登录 |
|  | menuAuthSignedInMsg | 您必须登录到{action} |
|  | menuUserEditProfile | 编辑个人资料 |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | 注销 |
|  | menuUserBackBtn | 所有 |

## 流信息{#section_wpy_gl4_xz}

可用于内容流信息和显示的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| “信息”菜单选项 | menuInfoCopyright | © Livefyre， Inc. 2014 |
|  | menuInfoHelp | 帮助 |
|  | menuInfoLivefyreLink | 访问Livefyre.com |

## 作者/内容信息{#section_dhb_gl4_xz}

可用于创作和单个内容信息。

| 元素 | 键 | 默认文本 |
|---|---|---|
|  | commentDrocidatTag | Mod |
|  | commentPendingTag | 待定 |
|  | commentReadMoreLink | 了解更多 |
|  | commentReplyLink | 请参阅{number}个回复 |
|  | commentReplyLinkSing | 查看回复 |
|  | commentVoteCount | 投票 |
|  | commentVoteCountSing | 票 |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | 数组. 默认 =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | questionExplanation | 现在，您可以直接阅读和写注释，包括句子、段落、图像和引号。<br><br><span class="&rdquo;lf-highlight-text&rdquo;">高亮</span> 显示文本， <span class="&rdquo;fycon-write&rdquo;"></span> 单击图标或 <span class="&rdquo;fycon-action-view&rdquo;"></span> 单击每个段落末尾的图标。 |
|  | questionMockText | “熟悉”的原因并不是众所周知，而是“熟悉”。 |
|  | questionTitle | 什么是Sithere? |

## 用户操作{#section_qxd_fl4_xz}

可用于用户操作的字符串：标记、共享和喜欢现有内容。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 回复菜单选项 | menuRepliesViewTitle | 详细信息 |
|  | menuRepliesViewReply | 回复对话 |
| 共享菜单选项 | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | 共享 |
| 标记菜单选项 | menuFlagOptionSarove | 反对 |
|  | menuFlagOptionOffension | 进攻 |
|  | menuFlagOptionOffTopic | 关闭主题 |
|  | menuFlagOptionSpam | 垃圾信息 |
|  | menuFlagTitle | 标志为…… |
|  | facebookShareCaption | “{title}”上的字号 |
| 移动用户选项 | sliderCommentTally | 的 |
|  | sliderInviteRead | 已读 |
|  | sliderInviteWrite | 写 |
|  | sliderLoading | 正在加载… |
|  | sliderWriteText | 你觉得呢？ 点击以写入。 |

## 帖子函数{#section_xzf_2l4_xz}

可用于发布内容的用户的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
|  | editorEditBtn | 保存 |
|  | editorEditPosting | 正在保存…… |
|  | editorEditReplyTitle | 编辑回复 |
|  | editorEditTitle | 编辑边线 |
|  | editorPlaceholder | 你觉得呢？ |
|  | editorPostBtn | 帖子字号 |
|  | editorPostBtnMobile | 帖子 |
|  | editorPosting | 正在发布… |
|  | editorReplyBtn | 回帖 |
|  | editorReplyTitle | 写回 |
|  | editorTitle | 写字符号 |
|  | emptyImageBlockTxt | 你觉得呢？ |
|  | emptyTextBlockTxt | + |
|  | replyBtn | 回复 |
|  | threadReplyBtn | 回复对话 |
| 删除菜单选项 | menuConfirmAccept | 是，{action} |
|  | menuConfirmCancel | 取消 |
|  | menuConfirmTitle | 是否确定？ |
| 等菜单选项 | menuEtcOptionApprove | 批准 |
|  | menuEtcOptionDelete | 删除 |
|  | menuEtcOptionEdit | 编辑 |
|  | menuEtcOptionFlag | 标记 |
|  | menuEtcOptionShare | 共享 |
|  | menuEtcPostedAt | 发布于{date} |
|  | menuEtcTitle | 更多 |

## 审查方接口{#section_o5f_dl4_xz}

可用于用户验证的审查方界面的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| “更多”菜单中的确认消息 | notificationApproved | 已批准 |
|  | notificationDeleted | 已删除 |
|  | notificationFlaged | 已标记 |

## 错误 {#section_gtk_cl4_xz}

可用于常规错误消息的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
|  | errorConnection | 哦哦。 你似乎没有好的联系。 |
|  | errorDuplicate | 我们也喜欢你的便条，但你不能发两遍。 |
|  | errorGeneral | 出现错误. 请重试。 |
|  | errorServer | 我们的服务器出了问题。 再试一次？ |
