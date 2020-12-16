---
description: 自定义Livefyre审阅的文本字符串。
seo-description: 自定义Livefyre审阅的文本字符串。
seo-title: 审阅文本字符串
solution: Experience Manager
title: 审阅文本字符串
uuid: 86251e49-bc73-4eec-9f9b-b4b0a5b42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 5%

---


# 查看文本字符串{#review-text-strings}

自定义Livefyre审阅的文本字符串。

本页列表和描述了可在审阅应用程序中自定义的字符串。 此处列出的字符串是Livefyre核心应用程序的默认字符串的附加字符串，并覆盖这些字符串，如字符串自定义中所列。 在列出重复时，这些表中列出的字符串是“审阅”应用程序的默认值。

实施
审阅／评级界面
流信息
作者／内容信息
用户操作
帖子功能
错误

## 实施 {#section-vsy-1k4-xz}

要实现此功能，请传递要覆盖的字符串的1-1对象映射到Javascript配置对象。 如果您不提供字段，将使用默认文本。

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

## 评论／评级接口{#section_iyv_zj4_xz}

可用于“审阅”和“评级”用户界面的字符串。

| 元素 | 键 | 默认文本 |
|--- |--- |--- |
| 按钮 | editReviewBtn | 编辑审阅 |
|  | reviewBtn | [编写审阅](https://d.pr/i/QscA) |
|  | reviewsClosed | [已结束审阅](https://d.pr/i/zr7M) |
|  | showReviewBtn | [显示审阅](https://d.pr/i/onxU) |
|  | 跟 | 我感兴趣 |
|  | shareText | 我刚写了个评论。 看看！ |
| 评级工具提示 | ratingValues | 数组. 默认值= `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`;<br>注意：必须复制数组中的值，才能将每颗星的左半部分和右半部分指定为同一名称。 |
| 分级子部件 | ratingSubpartPlaceholder | 数组. 默认 = `[]` |
|  | ratingSubpartTitles | 数组. 默认 = `[]` |
|  | reviewStreamTitle | 默认为空。 审阅摘要部分的标题。 |
| 杂项 | averageRating | [平均用户等级](https://d.pr/i/QscA) |
|  | breakdownHeader | [评级细分](https://d.pr/i/QscA) |
|  | 帮助 | %s(%s)发现有帮助 |
|  | hallibedPlural | %s(%s)发现有帮助 |
|  | outOf | / |
|  | ratingType | 星 |

## 流信息{#section_wmv_yj4_xz}

可用于内容流信息和显示的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 排序 | 排序依据 | 默认为空。 |
|  | sortHighestAdaded | [最高评级](https://d.pr/i/huTd) |
|  | sortNewstAdaided | [最低评级](https://d.pr/i/huTd) |
|  | sortMostHalliped | [最有用](https://d.pr/i/huTd) |
| 流杂项 | showMore | 显示更多 |
| 流高速 | newComment | 新建审阅 |
|  | newComments | 新评论 |
| 监听器计数 | listenerCount | 倾听 |
|  | listenerCountPlural | 倾听 |
| 评论计数 | commentCountLabel | LiveReviews<strong> | </strong> |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| 注释通知程序计数 | 注释通知程序 | 新建审阅 |
|  | commentNotifierPlural | 新评论 |

## 作者／内容信息{#section_osx_xj4_xz}

提供作者和个人内容信息。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 线程分组讨论 | reviewsContentNotFoundMsg | [此审阅不再可见](https://d.pr/i/svXs) |
|  | backToComments | 返回审阅 |

## 用户操作{#section_tlx_wj4_xz}

可用于用户操作的字符串：标记、共享和标记现有内容很有帮助。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 注释页脚 | wasReviewHalbed | [有帮助吗？](https://d.pr/i/Q0mA) |
|  | wasReviewHallipedMobile | 有帮助吗？ |
|  | ownWasReviewHalbed | [发现有帮助。](https://d.pr/i/Q0mA) |
|  | reviewWasHabled | [是](https://d.pr/i/Q0mA) |
|  | hallibedDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWasNotHalped | [否](https://d.pr/i/Q0mA) |
| 投票模式 | voteTitle | 此评论是否有用？ |
|  | voteDownvote | 否 |
|  | voteReplyTitle | 这个答案有帮助吗？ |
|  | voteTitle | 此评论有帮助吗？ |
|  | poteUpvote | 是 |
| 标志模式 | flagTitle | 标记%s的审阅 |
|  | flagSuccessMsg | 已标记审阅。 |
| 标记移动 | flagConfirmationMessage | 是否将%s的审阅标记为%s? |
| 提及模态 | 提及默认文本 | 我在Livefyre评论中提到过您！ |
| 共享模式 | shareTitle | 共享审阅 |

## 发布函数{#section_yl1_wj4_xz}

用于发布审阅的用户的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 编辑者 | bodyPlaceholder | 编写评论…… |
|  | postEditButton | 编辑 |
|  | postEditCancelButton | 取消 |
|  | postAsButton | 将审核发布为…… |
|  | postButton | 后审查 |
|  | postReplyAsButton | 发布为…… |
|  | postReplyButton | 帖子 |
|  | shareButton | 共享 |
|  | titlePlaceholder | 标题… |

## 错误 {#section_jbc_vj4_xz}

可用于常规错误消息的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 错误 | errorAlreadyPosted | 您只能发布一个审阅。 |
|  | errorAuthError | 您无权对此对话进行评论 |
|  | errorCommentsNotAllowed | 此时无法发布评论 |
|  | errorDiskleOwnComment | 你不能不喜欢自己的评论 |
|  | errorDuplicate | 尽管您喜欢评论，但您不得发布两次。 |
|  | errorEditDuplicate | 编辑审阅时，必须更改其正文。 |
|  | errorEditNotAllowed | 不允许您编辑此对话中的评论。 |
|  | errorEditTimeExceeded | 抱歉，您的审阅编辑期已过。 |
|  | errorEmpty | 您似乎在尝试发布空审阅。 |
|  | errorEmptyTitle | 您似乎在尝试发布空标题 |
|  | errorFieldRating | 星级 |
|  | errorFieldReview | 审查 |
|  | errorFieldTitle | title |
|  | errorMaxChars | 抱歉，您的评论太长。 请编辑，然后重试。 |
|  | errorMissingFields | 请输入 |
|  | errorRatingEmpty | 无法提交空评级 |
|  | errorRatingNotSet | 必须设置所有评级 |
|  | errorRatingNotValid | 等级必须为对象 |
|  | errorShowMore | 加载更多审阅时出错。 |
|  | errorTitleMaxChars | 抱歉，您的标题太长。 请编辑，然后重试。 |
|  | errorVoteOwnComment | 您不能对自己的审阅进行投票 |

