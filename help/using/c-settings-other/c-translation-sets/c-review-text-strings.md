---
description: 自定义Livefyre审阅的文本字符串。
title: 审阅文本字符串
exl-id: 82ced091-d573-4514-9b91-3451a94ed5d3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 5%

---

# 查看文本字符串{#review-text-strings}

自定义Livefyre审阅的文本字符串。

本页列表和描述了可在“审阅”应用程序中自定义的字符串。 此处列出的字符串是Livefyre核心应用程序的默认字符串的附加字符串，并覆盖这些字符串，这些字符串在字符串自定义中列出。 列出重复时，这些表中列出的字符串是“审阅”应用程序的默认值。

实施
审阅/评级界面
流信息
作者/内容信息
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

## 评论/评级接口{#section_iyv_zj4_xz}

可用于“审阅”和“评级”用户界面的字符串。

| 元素 | 键 | 默认文本 |
|--- |--- |--- |
| 按钮 | editReviewBtn | 编辑审阅 |
|  | reviewBtn | [编写审阅](https://d.pr/i/QscA) |
|  | reviewsClosed | [已结束审阅](https://d.pr/i/zr7M) |
|  | showReviewBtn | [显示审阅](https://d.pr/i/onxU) |
|  | flow | 我有兴趣 |
|  | shareText | 我刚写了个评论。 看看！ |
| 评级工具提示 | ratingValues | 数组. 默认值= `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`;<br>注意：必须复制数组中的值，才能将每颗星的左半和右半都指定相同的名称。 |
| 对子部件评级 | ratingSubpartPlaceholder | 数组. 默认 = `[]` |
|  | ratingSubpartTitles | 数组. 默认 = `[]` |
|  | reviewStreamTitle | 默认为空。 审阅摘要部分的标题。 |
| Misc | averageRating | [平均用户评级](https://d.pr/i/QscA) |
|  | breaklownHeader | [评级划分](https://d.pr/i/QscA) |
|  | 帮助 | %s(%s)发现有帮助 |
|  | halidePlural | %s(%s)发现有帮助 |
|  | outOf | / |
|  | ratingType | 星星 |

## 流信息{#section_wmv_yj4_xz}

可用于内容流信息和显示的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 排序 | sortBy | 默认为空。 |
|  | sortHighstAcaded | [最高评级](https://d.pr/i/huTd) |
|  | sortNewshAcadied | [最低评级](https://d.pr/i/huTd) |
|  | sortMostHalbide | [最有用](https://d.pr/i/huTd) |
| 流杂项 | showMore | 显示更多 |
| 流高速 | newComment | 新建审阅 |
|  | newComments | 新评论 |
| 侦听器计数 | listenerCount | 监听 |
|  | listenerCountPlural | 倾听 |
| 评论计数 | commentCountLabel | LiveReviews<strong> | </strong> |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| 注释通知程序计数 | commentNotifier | 新建审阅 |
|  | commentNotifierPlural | 新评论 |

## 作者/内容信息{#section_osx_xj4_xz}

可用于创作和单个内容信息。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 线程分组讨论 | reviewsContentNotFoundMsg | [此审阅不再可见](https://d.pr/i/svXs) |
|  | backToComments | 返回审阅 |

## 用户操作{#section_tlx_wj4_xz}

可用于用户操作的字符串：标记、共享和标记现有内容很有帮助。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 注释页脚 | wasReviewHalbed | [有帮助吗？](https://d.pr/i/Q0mA) |
|  | wasReviewHalbedMobile | 有帮助吗？ |
|  | ownWasReviewHalbide | [发现有帮助。](https://d.pr/i/Q0mA) |
|  | reviewWasHabled | [是](https://d.pr/i/Q0mA) |
|  | hallipedDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWasNotHalpid | [否](https://d.pr/i/Q0mA) |
| 投票模式 | voteTitle | 此评论有帮助吗？ |
|  | voteDownvote | 否 |
|  | voteReplyTitle | 这个回复有帮助吗？ |
|  | voteTitle | 此评论有帮助吗？ |
|  | voteUpvote | 是 |
| 旗标模式 | flagTitle | 标记%s的审阅 |
|  | flagSuccessMsg | 已标出审阅。 |
| 移动标志 | flagConfirmationMessage | 是否将%s的审阅标记为%s? |
| 提及模式 | untiteDefaultText | 我在Livefyre评论中提到过你！ |
| 共享模式 | shareTitle | 共享审阅 |

## 帖子函数{#section_yl1_wj4_xz}

可用于用户发布审阅的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 编辑者 | bodyPlaceholder | 写评论…… |
|  | postEditButton | 编辑 |
|  | postEditCancelButton | 取消 |
|  | postAsButton | 将审阅发布为…… |
|  | postButton | 帖子审阅 |
|  | postReplyAsButton | 发布为…… |
|  | postReplyButton | 帖子 |
|  | shareButton | 共享 |
|  | titlePlaceholder | 标题… |

## 错误 {#section_jbc_vj4_xz}

可用于常规错误消息的字符串。

| 元素 | 键 | 默认文本 |
|---|---|---|
| 错误 | errorAlreadedPosted | 您只能发布一次审阅。 |
|  | errorAuthError | 您无权对此对话进行评论 |
|  | errorCommentsNotAllowed | 此时无法发布审阅 |
|  | errorSdileOwnComment | 你不能不喜欢自己的评论 |
|  | errorDuplicate | 尽管你很喜欢你的评论，但你不能发布两次。 |
|  | errorEditDuplicate | 编辑审阅时，必须更改其正文。 |
|  | errorEditNotAllowed | 不允许您编辑此对话的评论。 |
|  | errorEditTimeExceeded | 抱歉，您的审阅编辑期已过。 |
|  | errorEmpty | 你似乎在尝试发布一个空白的评论。 |
|  | errorEmptyTitle | 你似乎在尝试发布一个空标题 |
|  | errorFieldRating | 星级 |
|  | errorFieldReview | 审查 |
|  | errorFieldTitle | title |
|  | errorMaxChars | 抱歉，您的评论太长。 请编辑并重试。 |
|  | errorMissingFields | 请输入 |
|  | errorRatingEmpty | 无法提交空评级 |
|  | errorRatingNotSet | 必须设置所有评级 |
|  | errorRatingNotValid | 评级必须为对象 |
|  | errorShowMore | 加载更多审阅时出错。 |
|  | errorTitleMaxChars | 抱歉，您的标题太长。 请编辑并重试。 |
|  | errorVoteOwnComment | 您不能对自己的审阅投票 |
