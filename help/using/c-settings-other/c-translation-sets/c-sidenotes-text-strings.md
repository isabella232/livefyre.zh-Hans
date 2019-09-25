---
description: 自定义Livefyre Sidesor的文本字符串
seo-description: 自定义Livefyre Sidesor的文本字符串
seo-title: 指示文本字符串
solution: Experience Manager
title: 指示文本字符串
uuid: a3735237-e55d-4bc0-b88d-8a323980ee09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# 指示文本字符串{#sidenotes-text-strings}

自定义Livefyre Sidesor的文本字符串

本页列出并描述了Sidesorps中可自定义的所有字符串。 有关核心Livefyre应用程序可用的字符串的信息，请参阅字符串自定义。

实施身份验证流信息作者／内容信息用户操作发布函数审查方界面错误

## 实施 {#section_wp2_ql4_xz}

要实现此功能，请传递要覆盖的字符串的1-1对象映射到Javascript配置对象。 如果不提供字段，则将使用默认文本。

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

## 身份验证 {#section_pqf_3l4_xz}

可用于身份验证过程的字符串，以及来自已验证用户菜单的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 身份验证菜单字符串 | menuAuthSignInBtn | 登录 |
|  | menuAuthSignedInMsg | 您必须登录到{action} |
|  | menuUserEditProfile | 编辑个人资料 |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | 注销 |
|  | menuUserBackBtn | 所有 |

## 流信息 {#section_wpy_gl4_xz}

可用于内容流信息和显示的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 信息菜单选项 | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | 帮助 |
|  | menuInfoLivefyreLink | 访问Livefyre.com |

## 作者／内容信息 {#section_dhb_gl4_xz}

提供作者和个人内容信息。

| 元素 | 键 | 默认文本 |
|---|---|---|
|  | commentDrocidatorTag | Mod |
|  | commentPendingTag | 待定 |
|  | commentReadMoreLink | 了解更多 |
|  | commentReplyLink | 请参阅{number}个回复 |
|  | commentReplyLinkSing | 查看回复 |
|  | commentVoteCount | 投票 |
|  | commentVoteCountSing | 票 |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | 数组. 默认 =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | questionExplanation | 您现在可以直接读写句子、段落、图像和引号上的注释。<br><br><span class="&rdquo;lf-highlight-text&rdquo;">高亮显示文本</span> ，然后单 <span class="&rdquo;fycon-write&rdquo;"></span> 击图标，或单 <span class="&rdquo;fycon-action-view&rdquo;"></span> 击每个段落末尾的图标。 |
|  | questionMockText | “熟悉”的内容并不清楚，原因是“熟悉”。 |
|  | questionTitle | 什么是Sithex? |

## 用户操作 {#section_qxd_fl4_xz}

可用于用户操作的字符串：标记、共享和喜欢现有内容。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 回复菜单选项 | menuRepliesViewTitle | 详细信息 |
|  | menuRepliesViewReply | 回复对话 |
| 共享菜单选项 | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | 共享 |
| 标记菜单选项 | menuFlagOptionSarove | 反对 |
|  | menuFlagOptionOffensive | 进攻性 |
|  | menuFlagOptionOffTopic | 关闭主题 |
|  | menuFlagOptionSpam | 垃圾信息 |
|  | menuFlagTitle | 标记为…… |
|  | facebookShareCaption | “{title}”上的字号 |
| 移动用户选项 | sliderCommentTally | 的 |
|  | sliderInviteRead | 已读 |
|  | sliderInviteWrite | 写 |
|  | sliderLoading | 正在加载… |
|  | sliderWriteText | 你觉得呢？ 点击以编写。 |

## 帖子功能 {#section_xzf_2l4_xz}

可用于发布内容的用户的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
|  | editorEditBtn | 保存 |
|  | editorEditPosting | 正在保存…… |
|  | editorEditReplyTitle | 编辑回复 |
|  | editorEditTitle | 编辑字号 |
|  | editorPlaceholder | 你觉得呢？ |
|  | editorPostBtn | 帖子表示 |
|  | editorPostBtnMobile | 帖子 |
|  | editorPosting | 正在发布… |
|  | editorReplyBtn | 回帖 |
|  | editorReplyTitle | 写回复 |
|  | editorTitle | 写字符号 |
|  | emptyImageBlockTxt | 你觉得呢？ |
|  | emptyTextBlockTxt | + |
|  | replyBtn | 回复 |
|  | threadReplyBtn | 回复对话 |
| 删除菜单选项 | menuConfirmAccept | 是，{action} |
|  | menuConfirmCancel | 取消 |
|  | menuConfirmTitle | 是否确定？ |
| 等等菜单选项 | menuEtcOptionApprove | 批准 |
|  | menuEtcOptionDelete | 删除 |
|  | menuEtcOptionEdit | 编辑 |
|  | menuEtcOptionFlag | 标记 |
|  | menuEtcOptionShare | 共享 |
|  | menuEtcPostedAt | 发布于{date} |
|  | menuEtcTitle | 更多 |

## 审查方界面 {#section_o5f_dl4_xz}

用户身份验证的审查方界面可用的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| “更多”菜单中的确认消息 | notificationApproved | 已批准 |
|  | notificationDeleted | 已删除 |
|  | notificationFlaged | 已标记 |

## 错误 {#section_gtk_cl4_xz}

可用于常规错误消息的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
|  | errorConnection | 哦。 您似乎没有良好的联系。 |
|  | errorDuplicate | 我们也喜欢您的便条，但您不能再发布一次。 |
|  | errorGeneral | 出现错误. 请重试。 |
|  | errorServer | 我们的服务器出了问题。 再试一次？ |

