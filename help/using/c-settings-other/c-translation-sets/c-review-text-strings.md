---
description: 自定义Livefyre审阅的文本字符串。
title: 查看文本字符串
exl-id: 82ced091-d573-4514-9b91-3451a94ed5d3
source-git-commit: 1d9088eecf797e1af881cb6be55b3c96284f75e5
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 5%

---

# 查看文本字符串{#review-text-strings}

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
| 子部件评级 | ratingSubpartPlaceholders | 数组. 默认 = `[]` |
|  | ratingSubpartTitles | 数组. 默认 = `[]` |
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
| 排序 | sortBy | 默认为空。 |
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
