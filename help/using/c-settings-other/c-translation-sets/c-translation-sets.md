---
description: 翻译集允许您为应用程序指定替代语言。
seo-description: 翻译集允许您为应用程序指定替代语言。
seo-title: 翻译集
solution: Experience Manager
title: 翻译集
uuid: 88b705e5-57c8-4065-8a41-a73546bd929a
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 翻译集{#translation-sets}

翻译集允许您为应用程序指定替代语言。

使用翻译设置本地化不同语言的应用程序，或从Studio中的一个位置为多个应用程序指定替代文本。 例如，您可以确保所有西班牙语站点对所有应用程序字段使用西班牙语。 您还可以修改文本，使所有字段都与站点或网络的语音和感觉相匹配。

您可以为除Storify 2之外的所有应用程序指定翻译设置。 有关可本地化哪些字段的详细信息，请参 [阅本地化字符串](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md#c-localize-strings)。

评论、实时博客和聊天在翻译集中共享同一组字符串。

为网络、站点、应用程序或使用API指定翻译集。

不同级别的翻译集会按照以下模式相互覆盖：

API翻译集将覆盖任何级别（应用程序、网络和站点）的任何翻译集应用程序翻译集将覆盖网络级和站点级翻译集。
站点级翻译集覆盖网络级翻译集。

## 审阅文本字符串 {#c_review_text_strings}

自定义Livefyre审阅的文本字符串。

本页列出并描述了在“审阅”应用程序中可进行自定义的字符串。 此处列出的字符串是Livefyre核心应用程序的默认字符串的附加字符串，并覆盖这些字符串，这些字符串在“字符串自定义”中列出。 在列出重复项的位置，这些表中列出的字符串是“审阅”应用程序的默认值。

实施审查／评级界面流信息作者／内容信息用户操作发布功能错误

## 实施 {#section-vsy-1k4-xz}

要实现此功能，请传递要覆盖的字符串的1-1对象映射到Javascript配置对象。 如果您不提供字段，则将使用默认文本。

示例：

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" }; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## 审阅／评级界面 {#section_iyv_zj4_xz}

可用于“审阅”和“评级”用户界面的字符串。

| 元素 | 键 | 默认文本 |
|--- |--- |--- |
| 按钮 | editReviewBtn | 编辑审阅 |
|  | reviewBtn | 编写审阅 |
|  | reviewsClosed | 已结束审阅 |
|  | showReviewBtn | 显示审阅 |
|  | flow | 我感兴趣 |
|  | shareText | 我刚写了个评论。 看看！ |
| 评级工具提示 | ratingValues | 数组. 默认值= `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; 注 <br>意：必须复制数组中的值，才能将每颗星的左半部分和右半部分指定为相同的名称。 |
| 等级子部分 | ratingSubpartPlaceholder | 数组. 默认 = [] |
|  | ratingSubpartTitles | 数组. 默认 = [] |
|  | reviewStreamTitle | 默认情况下为空。 审阅摘要部分的标题。 |
| Misc | averageRating | 平均用户评级 |
|  | breakdownHeader | 评级细分 |
|  | 帮助 | %s（已找到%s） |
|  | hallibedPlural | %s（已找到%s） |
|  | outOf | / |
|  | ratingType | 星星 |

## 流信息 {#section_wmv_yj4_xz}

可用于内容流信息和显示的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 排序 |  sortBy | *默认情况下为空。* |
|  | sortHighestRadied | [最高评级](https://d.pr/i/huTd) |
|  | sortNeethAdaided | [最低评级](https://d.pr/i/huTd) |
|  | sortMostHalpied | [最有帮助](https://d.pr/i/huTd) |
| 流杂项 | showMore | 显示更多 |
| 流高速 | newComment | 新评论 |
|  | newComments | 新评论 |
| 监听器计数 | listenerCount | 监听 |
|  | listenerCountPlural | 倾听 |
| 评论计数 | commentCountLabel | LiveReviews<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| 注释通知程序计数 | commentNotifier | 新评论 |
|  | commentNotifierPlural | 新评论 |

## 作者／内容信息 {#section_osx_xj4_xz}

提供作者和个人内容信息。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 线程分组讨论 | reviewsContentNotFoundMsg | [此审阅不再可见](https://d.pr/i/svXs) |
|  | backToComments | 返回审阅 |

## 用户操作 {#section_tlx_wj4_xz}

可用于用户操作的字符串：标记、共享和标记现有内容很有帮助。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 注释页脚 | wasReviewHalbid | [有帮助吗？](https://d.pr/i/Q0mA) |
|  | wasReviewHalbedMobile | 有帮助吗？ |
|  | ownWasReviewHallibed | [发现有帮助。](https://d.pr/i/Q0mA) |
|  | reviewWasHalbid | [是](https://d.pr/i/Q0mA) |
|  | hallibedDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWasNotHalpid | [否](https://d.pr/i/Q0mA) |
| 投票模式 | voteTitle | 此评论是否有用？ |
|  | voteDownvote | 否 |
|  | voteReplyTitle | 这个答复有帮助吗？ |
|  | voteTitle | 此评论有帮助吗？ |
|  | voteUpvote | 是 |
| 旗标模式 | flagTitle | 标记%s的审阅 |
|  | flagSuccessMsg | 已标记审阅。 |
| 标记移动 | flagConfirmationMessage | 是否将%s的审阅标记为%s? |
| 提及模态 | 提及DefaultText | 我在Livefyre评论中提到过您！ |
| 共享模式 | shareTitle | 共享审阅 |

## 帖子功能 {#section_yl1_wj4_xz}

可用于发布审阅的用户的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 编辑者 | bodyPlaceholder | 编写审阅…… |
|  | postEditButton | 编辑 |
|  | postEditCancelButton | 取消 |
|  | postAsButton | 将审阅发布为…… |
|  | postButton | 帖子评论 |
|  | postReplyAsButton | 发布为…… |
|  | postReplyButton | 帖子 |
|  | shareButton | 共享 |
|  | titlePlaceholder | 标题… |

## 错误 {#section_jbc_vj4_xz}

可用于常规错误消息的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 错误 | errorAlreadePosted | 您只能发布一个审阅。 |
|  | errorAuthError | 您无权对此对话发布评论 |
|  | errorCommentsNotAllowed | 此时无法发布评论 |
|  | errorDislokeOwnComment | 您不能不喜欢自己的审阅 |
|  | errorDuplicate | 尽管您喜欢评论，但您不得发布两次。 |
|  | errorEditDuplicate | 编辑审阅时，必须更改其正文。 |
|  | errorEditNotAllowed | 不允许您编辑此对话的评论。 |
|  | errorEditTimeExceeded | 抱歉，您的审阅编辑期已到期。 |
|  | errorEmpty | 您似乎在尝试发布空审阅。 |
|  | errorEmptyTitle | 您似乎在尝试发布空标题 |
|  | errorFieldRating | 星级 |
|  | errorFieldReview | 审查 |
|  | errorFieldTitle | title |
|  | errorMaxChars | 抱歉，您的评论太长。 请编辑并重试。 |
|  | errorMissingFields | 请输入 |
|  | errorRatingEmpty | 不能提交空评级 |
|  | errorRatingNotSet | 必须设置所有评级 |
|  | errorRatingNotValid | 等级必须为对象 |
|  | errorShowMore | 加载更多审阅时出错。 |
|  | errorTitleMaxChars | 抱歉，您的标题太长。 请编辑并重试。 |
|  | errorVoteOwnComment | 您不能对自己的审阅投票 |

## 指示文本字符串 {#c_sidenotes_text_strings}

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
|  | datetimeMonths | 数组. Default =[ ‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’ ] |
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

