---
description: 自定义Livefyre审阅的文本字符串。
seo-description: 自定义Livefyre审阅的文本字符串。
seo-title: 审阅文本字符串
solution: Experience Manager
title: 审阅文本字符串
uuid: 86251e49-bc73-4eec-9f9b-b4b0a5b42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# 审阅文本字符串{#review-text-strings}

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
|  | reviewBtn | [编写审阅](https://d.pr/i/QscA) |
|  | reviewsClosed | [已结束审阅](https://d.pr/i/zr7M) |
|  | showReviewBtn | [显示审阅](https://d.pr/i/onxU) |
|  | flow | 我感兴趣 |
|  | shareText | 我刚写了个评论。 看看！ |
| 评级工具提示 | ratingValues | 数组. 默认值= `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; 注 <br>意：必须复制数组中的值，才能将每颗星的左半部分和右半部分指定为相同的名称。 |
| 等级子部分 | ratingSubpartPlaceholder | 数组. 默认 = `[]` |
|  | ratingSubpartTitles | 数组. 默认 = `[]` |
|  | reviewStreamTitle | 默认情况下为空。 审阅摘要部分的标题。 |
| Misc | averageRating | [平均用户评级](https://d.pr/i/QscA) |
|  | breakdownHeader | [评级细分](https://d.pr/i/QscA) |
|  | 帮助 | %s（已找到%s） |
|  | hallibedPlural | %s（已找到%s） |
|  | outOf | / |
|  | ratingType | 星星 |

## 流信息 {#section_wmv_yj4_xz}

可用于内容流信息和显示的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 排序 |  sortBy | 默认情况下为空。 |
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

