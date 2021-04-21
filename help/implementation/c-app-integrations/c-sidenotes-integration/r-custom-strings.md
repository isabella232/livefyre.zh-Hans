---
title: Siestors自定义字符串
description: Siestors自定义字符串
exl-id: b5e2c18b-5b98-45ff-aa89-dd92a02949a9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 12%

---

# Siestraver Custom Strings{#sidenotes-custom-strings}

自定义字符串通过注入到Siser构造函数中的对象应用，并覆盖通过应用程序使用的默认字符串。 这些组件可用于自定义语言的任何部分以适合您的样式或语言规范。 字符串将自动与默认值合并。

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| 键 | 默认 |
|---|---|
| appName | Siestr |
| commentDrocidatTag | Mod |
| commentPendingTag | 待定 |
| commentReadMoreLink | 了解更多 |
| commentReplyLink | 请参阅{number}个回复 |
| commentReplyLinkSing | 查看回复 |
| commentVoteCount | 投票 |
| commentVoteCountSing | 票 |
| editorPlaceholder | 你觉得呢？ |
| editorPostBtn | 帖子字号 |
| editorPostBtnMobile | 帖子 |
| editorPosting | 正在发布… |
| editorReplyBtn | 回帖 |
| editorReplyTitle | 写回 |
| editorTitle | 写注释 |
| emptyImageBlockTxt | 你觉得呢？ |
| emptyTextBlockTxt | + |
| errorConnection | 哦哦。 你似乎没有好的联系。 |
| errorDuplicate | 我们也喜欢你的便条，但你不能发两遍。 |
| errorGeneral | 出现错误. 请重试。 |
| errorServer | 我们的服务器出了问题。 再试一次？ |
| facebookShareCaption | “{title}”上的SideNotes |
| menuAuthSignedInMsg | 您必须登录到{action} |
| menuAuthSignInBtn | 登录 |
| menuBackBtn | 返回 |
| menuConfirmAccept | 是，{action} |
| menuConfirmCancel | 取消 |
| menuConfirmTitle | 是否确定？ |
| menuEtcOptionApprove | 批准 |
| menuEtcOptionDelete | 删除 |
| menuEtcOptionEdit | 编辑 |
| menuEtcOptionFlag | 标记 |
| menuEtcOptionShare | 共享 |
| menuEtcPostedAt | 发布于{date} |
| menuEtcTitle | 更多 |
| menuFlagOptionSarove | 反对 |
| menuFlagOptionOffension | 进攻 |
| menuFlagOptionOffTopic | 关闭主题 |
| menuFlagOptionSpam | 垃圾信息 |
| menuFlagTitle | 标志为…… |
| menuInfoCopyright | © Livefyre， Inc. 2014 |
| menuInfoHelp | 帮助 |
| menuInfoLivefyreLink | 访问Livefyre.com |
| menuRepliesViewReply | 回复对话 |
| menuRepliesViewTitle | 详细信息 |
| menuShareOptionFacebook | Facebook |
| menuShareOptionLink | 复制Permalink |
| menuShareOptionLinkComplete | 已复制 |
| menuShareOptionLinkFailed | 复制失败 |
| menuShareOptionTwitter | Twitter |
| menuShareTitle | 共享 |
| notificationApproved | 已批准 |
| notificationDeleted | 已删除 |
| notificationFlaged | 已标记 |
| permalinkBackBtn | 所有 |
| permalinkTitle | 佩马林克 |
| questionExplanation | 现在，您可以直接阅读和写注释，包括句子、段落、图像和引号。<br><br>高亮显示文本，单击每段末尾的“fycon-write”图标或“fycon-action-视图”图标。 |
| questionMockText | “熟悉”的原因并不是众所周知，而是“熟悉”。 |
| questionTitle | 什么是Sithere? |
| queedCommentsPlural | {number}新增大小 |
| queuedCommentsSingular | 1个新字符 |
| queuedRepliesPlural | {number}个新回复 |
| queuedRepliesSingular | 1个新回复 |
| replyBtn | 回复 |
| signInToPost | 登录以写字符 |
| sliderCommentTally | 的 |
| sliderInviteRead | 已读 |
| sliderInviteWrite | 写 |
| sliderWriteText | 你觉得呢？ 点击以写入 |
| threadCollapseBtn | 折叠 |
| threadExpandBtnPlural | 展开{number}个回复 |
| threadExpandBtnSingular | 展开1个回复 |
| threadReplyBtn | 回复对话 |
