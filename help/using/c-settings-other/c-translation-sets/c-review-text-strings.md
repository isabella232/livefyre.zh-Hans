---
description: 自定义Livefyre审阅的文本字符串。
seo-description: 自定义Livefyre审阅的文本字符串。
seo-title: 审阅文本字符串
solution: Experience Manager
title: 审阅文本字符串
uuid: 86251e49-bc73-4eec-9f9 b-b4 b0 a5 b42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# 审阅文本字符串{#review-text-strings}

自定义Livefyre审阅的文本字符串。

此页面列出并描述了可在审核应用程序中自定义的字符串。此处列出的字符串还为Livefyre核心应用程序的默认字符串以及字符串自定义中列出的默认字符串。列出重复项时，这些表中列出的字符串是评论应用程序的默认值。

实施审阅/分级界面流信息作者/内容信息用户操作帖子功能错误

## 实施 {#section-vsy-1k4-xz}

要执行此功能，请传递要覆盖到Javascript配置对象的字符串的一个-1对象映射。如果不提供字段，将使用默认文本。

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

## 审阅/评级界面 {#section_iyv_zj4_xz}

可用于审核和评级用户界面的字符串。

| Element | Key | 默认文本 |
|--- |--- |--- |
| 按钮 | editReviewBtn | 编辑评论 |
|  | reviewBtn | [编写评论](https://d.pr/i/QscA) |
|  | reviewsClosed | [已关闭审阅](https://d.pr/i/zr7M) |
|  | showReviewBtn | [显示评论](https://d.pr/i/onxU) |
|  | 关注 | 我很感兴趣 |
|  | ShareText | 我刚刚编写了评论。来看一看吧！ |
| 评级工具提示 | RatingValues | 数组。默认= `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`； <br>注意：必须重复数组中的值，以将每个星形的左侧和右半部分分配给同一个名称。 |
| 评级子部分 | RatingSubpartplaceHolders | 数组。默认值= `[]` |
|  | RatingSubpartTitles | 数组。默认值= `[]` |
|  | reviewStreamTitle | 默认为空。评论摘要部分的标题。 |
| Misc | 平均值创建 | [平均用户等级](https://d.pr/i/QscA) |
|  | BreakDownHeader | [评级细分](https://d.pr/i/QscA) |
|  | 有帮助 | %s的%s发现有帮助 |
|  | HelpFulcomple | %s的%s发现有帮助 |
|  | Of Of | / |
|  | RatingType | 星形 |

## 流信息 {#section_wmv_yj4_xz}

可用于内容流信息和显示的字符串。

| Element | Key | 默认文本 |
|---|---|---|
| 排序 | SortBy | 默认为空。 |
|  | Sorthighead | [最高评级](https://d.pr/i/huTd) |
|  | SortLoweSoft | [最低评级](https://d.pr/i/huTd) |
|  | SortmosThelpul | [最有帮助的](https://d.pr/i/huTd) |
| 流错误。 | Showmore | 显示更多 |
| 流高速 | NewComment | 新评论 |
|  | News Comments | 新评论 |
| 监听器计数 | listenerCount | 人物监听 |
|  | listenerCountMultiple | 用户聆听 |
| 注释计数 | commentCountLabel | LivereViews<strong> | </strong>%s |
|  | CommentCountLabelMultiple | LivereViews<strong> | </strong>%s |
| 注释通知计数 | CommentNotifier | 新评论 |
|  | CommentNotifierMultiple | 新评论 |

## 作者/内容信息 {#section_osx_xj4_xz}

可用于创作和个人内容信息。

| Element | Key | 默认文本 |
|---|---|---|
| 线程分组讨论 | reviewsContentNotFoundMsg | [此审阅不再可见](https://d.pr/i/svXs) |
|  | 背景注释 | 返回审阅 |

## 用户操作 {#section_tlx_wj4_xz}

可用于用户操作的字符串：标记、共享和标记现有内容非常有用。

| Element | Key | 默认文本 |
|---|---|---|
| 评论页脚 | wasreviewHelpful | [有帮助？](https://d.pr/i/Q0mA) |
|  | wasreviewHilpFulmobile | 有帮助？ |
|  | ownwasreviewHelpful | [发现有用。](https://d.pr/i/Q0mA) |
|  | ReviewWasHelp | [是](https://d.pr/i/Q0mA) |
|  | HelpFuldider | [&amp; amp；vert；](https://d.pr/i/Q0mA) |
|  | ReviewWasnotHelpul | [否](https://d.pr/i/Q0mA) |
| 投票模式 | VOTitle | 此审阅是否有用？ |
|  | 技术投票 | 否 |
|  | vterePlyTitle | 此回复是否有用？ |
|  | VOTitle | 此注释是否有用？ |
|  | VoTeup投票 | 是 |
| 标记模式 | Flagtitle | 标记%s的审阅 |
|  | FlagsuccessMsg | 已对审阅进行了标记。 |
| Flag Mobile | 标记确认消息 | 将%s的审阅标记为%s？ |
| 提及模式 | mentionDefaultText | 我在Livefyre审阅中提及了您！ |
| 共享模式 | ShareTitle | 共享审阅 |

## 发布函数 {#section_yl1_wj4_xz}

可供用户发布评论的字符串。

| Element | Key | 默认文本 |
|---|---|---|
| 编辑者 | bodyplaceHolder | 编写评论… |
|  | PostEditButton | 编辑 |
|  | PostEditSeButton | 取消 |
|  | PostSutton | 将审阅发布为… |
|  | PostButton | 发布评论 |
|  | podStreplasButton | 发布为… |
|  | podStreplyButton | Post |
|  | ShareButton | Share |
|  | titleplaceHolder | 标题… |

## 错误 {#section_jbc_vj4_xz}

可用于一般错误消息的字符串。

| Element | Key | 默认文本 |
|---|---|---|
| 错误 | ErroralreadyPublished | 您只能发布一个审阅。 |
|  | ErrorAutoError | 您无权在此对话中发表评论 |
|  | errorcommentsNowAllowed | 此时无法发布评论 |
|  | 错误的注释 | 您不能喜欢自己的审阅 |
|  | ErrorDuplicate | 只要您喜欢审阅，就不能再将其发布两次。 |
|  | ErrorEditDuplicate | 编辑时，必须更改审阅的正文。 |
|  | errorEditNowAllowed | 您不能编辑此对话的评论。 |
|  | errorEditTime已超出 | 抱歉，您的审阅编辑期已过期。 |
|  | errorEmpty | 似乎您正在尝试发布空审阅。 |
|  | errorempty标题 | 好像您正在尝试发布空标题 |
|  | errorField | 星形评级 |
|  | ErrorField审阅 | review |
|  | errorField标题 | title |
|  | errorMaxChars | 抱歉，您的审阅太长了。请编辑并重试。 |
|  | errorMissingFields | 请输入 |
|  | errorRatingEmpty | 您无法提交空评级 |
|  | ErrorRatingNotSet | 必须设置所有评级 |
|  | errorRatingNotValid | 评级必须是对象 |
|  | ErrorShowmore | 加载更多评论时出错。 |
|  | ErrortitlamaChars | 抱歉，您的标题太长了。请编辑并重试。 |
|  | 错误注释 | 您无法根据自己的审阅投票 |

