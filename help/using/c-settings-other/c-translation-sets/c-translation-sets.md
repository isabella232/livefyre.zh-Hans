---
description: 翻译集允许您为应用程序指定替代语言。
title: 翻译集
exl-id: 1de99602-b97e-42e9-8450-39abd4ba2f9b
source-git-commit: 1d9088eecf797e1af881cb6be55b3c96284f75e5
workflow-type: tm+mt
source-wordcount: '1294'
ht-degree: 7%

---

# 翻译集{#translation-sets}

翻译集允许您为应用程序指定替代语言。

使用翻译设置将各种语言的应用程序本地化，或在Studio中的一个位置为多个应用程序指定替换文本。 例如，您可以确保所有西班牙语网站在所有应用程序字段中都使用西班牙语。 您还可以修改文本，以便所有字段都与您网站或网络的语音和感觉相匹配。

您可以为除Storify 2之外的所有应用程序指定翻译设置。 有关可本地化哪些字段的更多信息，请参阅[本地化字符串](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md#c-localize-strings)。

评论、实时博客和聊天在翻译集中共享相同的字符串集。

为网络、站点、应用程序或使用API指定翻译集。

不同级别的翻译集会按照以下模式相互覆盖：

API翻译集会覆盖任何级别（应用程序、网络和站点）的任何翻译集
应用程序翻译集会覆盖网络级别和站点级别的翻译集。
站点级翻译集覆盖网络级翻译集。

## 查看文本字符串 {#c_review_text_strings}

自定义Livefyre审阅的文本字符串。

本页列出并描述了可在审核应用程序中进行自定义的字符串。 此处列出的字符串是Livefyre核心应用程序的默认字符串的补充和覆盖，这些字符串在字符串自定义中列出。 其中列出了重复项，这些表中列出的字符串是“审阅”应用程序的默认字符串。

实施
审核/评级界面
流信息
作者/内容信息
用户操作
帖子函数
错误

## 实施 {#section-vsy-1k4-xz}

要实施此功能，请传入要覆盖的字符串的1-1对象映射到Javascript配置对象。 如果未提供字段，则将使用默认文本。

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

## 审核/评级界面 {#section_iyv_zj4_xz}

可用于“审阅”和“评级”用户界面的字符串。

| 元素 | 键 | 默认文本 |
|--- |--- |--- |
| 按钮 | editReviewBtn | 编辑审阅 |
|  | reviewBtn | 写审阅 |
|  | reviewsClosed | 已结束审阅 |
|  | showReviewBtn | 显示审阅 |
|  | 关注 | 我感兴趣 |
|  | shareText | 我刚写了个评论。 看看！ |
| 评分工具提示 | ratingValues | 数组. 默认值= `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`;<br>注意：必须复制数组中的值，才能将每颗星的左半部分和右半部分均指定相同的名称。 |
| 子部件评级 | ratingSubpartPlaceholders | 数组. 默认 = [] |
|  | ratingSubpartTitles | 数组. 默认 = [] |
|  | reviewStreamTitle | 默认为空。 评论摘要部分的标题。 |
| 杂项 | averageRating | 平均用户评分 |
|  | breakdownHeader | 评级划分 |
|  | 帮助 | %s(%s)发现有帮助 |
|  | halditedPlural | %s(%s)发现有帮助 |
|  | outOf | / |
|  | ratingType | 星星 |

## 流信息 {#section_wmv_yj4_xz}

可用于内容流信息和显示的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 排序 | sortBy | *默认为空。* |
|  | sortHieghtAded | 最高评级 |
|  | sortLewstAraded | 最低评级 |
|  | sortMostHampited | 最有用 |
| 流杂项。 | showMore | 显示更多 |
| 流高速 | newComment | 新审阅 |
|  | newComments | 新评论 |
| 监听程序计数 | listenerCount | 侦听 |
|  | listenerCountPlural | 倾听 |
| 评论计数 | commentCountLabel | LiveReviews<strong> | </strong> |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| 注释通告程序计数 | commentNotifier | 新审阅 |
|  | commentNotifierPlural | 新评论 |

## 作者/内容信息 {#section_osx_xj4_xz}

可用于创作和单个内容信息的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 线程中断 | reviewsContentNotFoundMsg | 此审阅不再可见 |
|  | backToComments | 返回审阅 |

## 用户操作 {#section_tlx_wj4_xz}

可用于用户操作的字符串：标记、共享和标记现有内容很有帮助。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 注释页脚 | wasReviewHalped | 有用吗？ |
|  | wasReviewHalbedMobile | 有用吗？ |
|  | ownWasReviewHampited | 发现有用。 |
|  | reviewWasHalpid | 是 |
|  | hallideDivider | &amp;vert; |
|  | reviewWasNotHalped | 否 |
| 投票模式 | voteTitle | 此审阅是否有帮助？ |
|  | voteDownvote | 否 |
|  | voteReplyTitle | 此回复有用吗？ |
|  | voteTitle | 此评论有用吗？ |
|  | voteUpvote | 是 |
| 标志模式 | flagTitle | 标记%s的审阅 |
|  | flagSuccessMsg | 已标记审核。 |
| 标记移动 | flagConfirmationMessage | 是否将%s的审阅标记为%s? |
| 提及模式窗口 | tunticeDefaultText | 我在Livefyre评论中提过你！ |
| 共享模式窗口 | shareTitle | 共享审阅 |

## 帖子函数 {#section_yl1_wj4_xz}

可用于用户发布审阅的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 编辑者 | bodyPlaceholder | 写评论…… |
|  | postEditButton | 编辑 |
|  | postEditCancelButton | 取消 |
|  | postAsButton | 审核后为…… |
|  | postButton | 帖子审阅 |
|  | postReplyAsButton | 发布为…… |
|  | postReplyButton | 帖子 |
|  | shareButton | 共享 |
|  | titlePlaceholder | 标题… |

## 错误 {#section_jbc_vj4_xz}

可用于常规错误消息的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 错误 | errorAlreadyPosted | 您只能发布一次审核。 |
|  | errorAuthError | 您无权发布对此对话的评论 |
|  | errorCommentsNotAllowed | 此时无法发布评论 |
|  | errorDislikeOwnComment | 你不能不喜欢自己的评论 |
|  | errorDuplicate | 尽管你喜欢评论，但是你不得发布两次。 |
|  | errorEditDuplicate | 编辑审阅时必须更改审阅正文。 |
|  | errorEditNotAllowed | 不允许您编辑此对话的评论。 |
|  | errorEditTimeExceeded | 很抱歉，您的审阅编辑期限已过期。 |
|  | errorEmpty | 你似乎在尝试发布空的评论。 |
|  | errorEmptyTitle | 你似乎想发布一个空标题 |
|  | errorFieldRating | 星级评级 |
|  | errorFieldReview | 审查 |
|  | errorFieldTitle | title |
|  | errorMaxChars | 抱歉，您的审阅太长。 请编辑并重试。 |
|  | errorMissingFields | 请输入 |
|  | errorRatingEmpty | 您无法提交空评级 |
|  | errorRatingNotSet | 必须设置所有评级 |
|  | errorRatingNotValid | 评级必须是对象 |
|  | errorShowMore | 加载更多审阅时出错。 |
|  | errorTitleMaxChars | 抱歉，您的标题太长。 请编辑并重试。 |
|  | errorVoteOwnComment | 你不能对自己的评论投票 |

## 字符串表示文本字符串 {#c_sidenotes_text_strings}

自定义Livefyre Sidenotes的文本字符串

本页列出并描述了Sidenotes应用程序中可进行自定义的所有字符串。 有关核心Livefyre应用程序可用的字符串的信息，请参阅字符串自定义。

实施
身份验证
流信息
作者/内容信息
用户操作
帖子函数
审核者界面
错误

## 实施 {#section_wp2_ql4_xz}

要实施此功能，请传入要覆盖的字符串的1-1对象映射到Javascript配置对象。 如果未提供字段，则将使用默认文本。

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

可用于身份验证过程和已验证用户菜单的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 身份验证菜单字符串 | menuAuthSignInBtn | 登录 |
|  | menuAuthSignedInMsg | 必须登录到{action} |
|  | menuUserEditProfile | 编辑个人资料 |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | 注销 |
|  | menuUserBackBtn | 所有 |

## 流信息 {#section_wpy_gl4_xz}

可用于内容流信息和显示的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| “信息”菜单选项 | menuInfoCopyright | © Livefyre， Inc. 2014 |
|  | menuInfoHelp | 帮助 |
|  | menuInfoLivefyreLink | 访问Livefyre.com |

## 作者/内容信息 {#section_dhb_gl4_xz}

可用于创作和单个内容信息的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
|  | commentDreciduatTag | Mod |
|  | commentPendingTag | 待定 |
|  | commentReadMoreLink | 了解更多 |
|  | commentReplyLink | 请参阅{number}个回复 |
|  | commentReplyLinkSing | 请参阅回复 |
|  | commentVoteCount | 投票 |
|  | commentVoteCountSing | 票 |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | 数组. 默认=[ &#39;January&#39;、&#39;二月&#39;、&#39;March&#39;、&#39;April&#39;、&#39;May&#39;、&#39;June&#39;、&#39;July&#39;、&#39;August&#39;、&#39;Sjept&#39;、&#39;Oncume&#39;、&#39;Rovel&#39;、&#39;Racken&#39;、&#39;Racker&#39; ] |
|  | questionExplation | 现在，您可以直接在句子、段落、图像和引号中读取和写入评论。<br><br><span class="&rdquo;lf-highlight-text&rdquo;">突出</span> 显示文本，然 <span class="&rdquo;fycon-write&rdquo;"></span> 后单击图标，或 <span class="&rdquo;fycon-action-view&rdquo;"></span> 者单击每个段落末尾的图标。 |
|  | questionMockText | “熟悉”的内容并不为人所知，只是因为它“熟悉”。 |
|  | questionTitle | 什么是Sidexer? |

## 用户操作 {#section_qxd_fl4_xz}

可用于用户操作的字符串：标记、共享和称赞现有内容。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 回复菜单选项 | menuRepliesViewTitle | 详细信息 |
|  | menuRepliesViewReply | 回复对话 |
| 共享菜单选项 | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | 共享 |
| 标记菜单选项 | menuFlagOptionDecover | 不同意 |
|  | menuFlagOptionOffensive | 进攻 |
|  | menuFlagOptionOffTopic | 关闭主题 |
|  | menuFlagOptionSpam | 垃圾信息 |
|  | menuFlagTitle | 标记为…… |
|  | facebookShareCaption | “{title}”上的Sidenotes |
| 移动设备用户选项 | sliderCommentTally | 的 |
|  | sliderInviteRead | 已读 |
|  | sliderInviteWrite | 写入 |
|  | sliderLoading | 正在加载… |
|  | sliderWriteText | 你觉得呢？ 点按以写入。 |

## 帖子函数 {#section_xzf_2l4_xz}

可用于发布内容的用户的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
|  | editorEditBtn | 保存 |
|  | editorEditPosting | 正在保存…… |
|  | editorEditReplyTitle | 编辑回复 |
|  | editorEditTitle | 编辑表示 |
|  | editorPlaceholder | 你觉得呢？ |
|  | editorPostBtn | 后表示 |
|  | editorPostBtnMobile | 帖子 |
|  | editorPosting | 正在发布… |
|  | editorReplyBtn | 回帖 |
|  | editorReplyTitle | 写回复 |
|  | editorTitle | 写字表示 |
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
|  | menuEtcPostedAt | 发布日期： {date} |
|  | menuEtcTitle | 更多 |

## 审核者界面 {#section_o5f_dl4_xz}

用户验证审核者界面可用的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 通过“更多”菜单确认消息 | notificationApproved | 已批准 |
|  | notificationDeleted | 已删除 |
|  | notificationFraged | 已标记 |

## 错误 {#section_gtk_cl4_xz}

可用于常规错误消息的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
|  | errorConnection | 哦。 你似乎没有好的联系。 |
|  | errorDuplicate | 我们也喜欢你的便条，但你不能发两遍。 |
|  | errorGeneral | 出现错误. 请重试。 |
|  | errorServer | 我们的服务器出了问题。 再试一次？ |
