---
description: 翻译集允许您为应用程序指定替代语言。
seo-description: 翻译集允许您为应用程序指定替代语言。
seo-title: 翻译集
solution: Experience Manager
title: 翻译集
uuid: 88b705e5-57c 8-4065-a41-a73546 bd929 a
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 翻译集{#translation-sets}

翻译集允许您为应用程序指定替代语言。

使用翻译设置本地化各种语言的应用程序，或在Studio中的一个位置指定多个应用程序的替代文本。例如，您可以确保所有西班牙语站点都使用西班牙语语言用于所有应用程序字段。您还可以修改文本，使所有字段与站点或网络的语音和感觉相匹配。

可为除Storify之外的所有应用程序指定翻译设置。有关可以本地化的字段的详细信息，请参阅 [本地化字符串](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md#c-localize-strings)。

注释、Live Blog和聊天在一个翻译集中共享同一组字符串。

指定网络、站点、应用程序或API的翻译集。

不同级别的翻译集按照以下模式相互覆盖：

API转换集覆盖任何级别的任何翻译集(应用程序、网络和站点)应用程序翻译集覆盖网络级别和站点级翻译集。
站点级翻译集覆盖网络级翻译集。

## 审阅文本字符串 {#c_review_text_strings}

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
|  | reviewBtn | 编写评论 |
|  | reviewsClosed | 已关闭审阅 |
|  | showReviewBtn | 显示评论 |
|  | 关注 | 我很感兴趣 |
|  | ShareText | 我刚刚编写了评论。来看一看吧！ |
| 评级工具提示 | RatingValues | 数组。默认= `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`； <br>注意：必须重复数组中的值，以将每个星形的左侧和右半部分分配给同一个名称。 |
| 评级子部分 | RatingSubpartplaceHolders | 数组。默认值= [] |
|  | RatingSubpartTitles | 数组。默认值= [] |
|  | reviewStreamTitle | 默认为空。评论摘要部分的标题。 |
| Misc | 平均值创建 | 平均用户等级 |
|  | BreakDownHeader | 评级细分 |
|  | 有帮助 | %s的%s发现有帮助 |
|  | HelpFulcomple | %s的%s发现有帮助 |
|  | Of Of | / |
|  | RatingType | 星形 |

## 流信息 {#section_wmv_yj4_xz}

可用于内容流信息和显示的字符串。

| Element | Key | 默认文本 |
|---|---|---|
| 排序 | SortBy | *默认为空。* |
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
|  | HelpFuldider | [& amp；vert；](https://d.pr/i/Q0mA) |
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

## Sid表示文本字符串 {#c_sidenotes_text_strings}

自定义LivefyreSiten说明的文本字符串

此页面列出并描述了在SiteNote应用程序中可自定义的所有字符串。有关可用于核心Livefyre应用程序的字符串的信息，请参阅字符串自定义。

实施Ah
Stream Info
Author/Content Info用户操作帖子函数审核器界面错误

## 实施 {#section_wp2_ql4_xz}

要执行此功能，请传递要覆盖到Javascript配置对象的字符串的一个-1对象映射。如果不提供字段，则将使用默认文本。

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

可用于身份验证过程的字符串以及经过身份验证的用户菜单。

| Element | Key | 默认文本 |
|---|---|---|
| Auth菜单字符串 | menuAuthSignInBtn | 登录 |
|  | MenuAuthesignMsg | 您必须登录{action} |
|  | menuUserEditProfile | 编辑配置文件 |
|  | menuusermin | Admin Console |
|  | menuUserLogout | 注销 |
|  | menuUserBackBtn | 全部 |

## 流信息 {#section_wpy_gl4_xz}

可用于内容流信息和显示的字符串。

| Element | Key | 默认文本 |
|---|---|---|
| “信息”菜单选项 | menuInFocoCopyright | © Livefyre，Inc2014 |
|  | menuInfoHelp | 帮助 |
|  | menuInfolveFileLink | 访问Livefyre.com |

## 作者/内容信息 {#section_dhb_gl4_xz}

可用于创作和个人内容信息。

| Element | Key | 默认文本 |
|---|---|---|
|  | CommentModeratorTag | Mod |
|  | 注释标记 | 待定 |
|  | 注释自述链接 | 阅读更多 |
|  | 注释链接 | 请参阅{number}回复 |
|  | 注释链接 | 请参阅回复 |
|  | CommentVoeCount | 投票 |
|  | 注释技术 | 投票 |
|  | dateTimmanuutPrefix | m m |
|  | DateTimeMonthths | 数组。默认=[ “月”、“二月”、“月”、“四月”、“五月”、“六月”、“月”、“月”、“九月”、“十月”、“十一月”、“十二月”、“十二月” ] |
|  | 问题解释 | 您现在可以直接在句子、段落、图像和引号上阅读和编写注释。<br><br><span class="&rdquo;lf-highlight-text&rdquo;">突出显示文本</span> 并单击 <span class="&rdquo;fycon-write&rdquo;"></span> 图标，或单击每个段落末尾的 <span class="&rdquo;fycon-action-view&rdquo;"></span> 图标。 |
|  | 问题模型 | “熟悉的知识”是不正确的，只是因为它是“熟悉”的原因。 |
|  | 问题标题 | 什么是Sitenote？ |

## 用户操作 {#section_qxd_fl4_xz}

可用于用户操作的字符串：标记、共享和称赞现有内容。

| Element | Key | 默认文本 |
|---|---|---|
| 回复菜单选项 | menuRepliciesViewTitle | 详细信息 |
|  | menuRepliciesView回复 | 回复对话 |
| 共享菜单选项 | MenuShareOptionFacebook | Facebook |
|  | MenuShareOptionTwitter | Twitter |
|  | MenuShareTitle | Share |
| 旗标菜单选项 | 菜单标记反对 | 反对 |
|  | MenuFlagoptionOfficy | 攻击性 |
|  | menuFlagoptionOffTopic | 关闭主题 |
|  | MenuFlagoptionSpam | 垃圾信息 |
|  | menuFlagtitle | 标记为… |
|  | FacebookShareCaption | Sidenes on“{title}” |
| 移动用户选项 | 幻灯片评论 | of |
|  | SliderInviteRead | 阅读阅读 |
|  | SliderInviteWrite | Write |
|  | 幻灯片加载 | 正在加载… |
|  | sliderWriteText | 您想什么？点击以写入。 |

## 发布函数 {#section_xzf_2l4_xz}

可供用户发布内容的字符串。

| Element | Key | 默认文本 |
|---|---|---|
|  | editorEditBtn | Save |
|  | 编辑编辑窗格 | 正在保存… |
|  | editorEditReplicyTitle | 编辑回复 |
|  | 编辑编辑标题 | 编辑Siennote |
|  | editorPlaceHolder | 您想什么？ |
|  | editorPostBtn | 发布站点 |
|  | EditorPostBtnsMobile | Post |
|  | 编辑窗格 | 发布… |
|  | editorReplicBtn | 回复回复 |
|  | editorReplicitTitle | 回复回复 |
|  | 编辑标题 | 写入Sienote |
|  | emptyImageBlockxt | 您想什么？ |
|  | emptyTextBlockXT | + |
|  | replicyBtn | Reply |
|  | searchReplicBtn | 回复对话 |
| 删除菜单选项 | menuConfirmAc接受 | 是，{action} |
|  | menuConfirmCancel | 取消 |
|  | menuConfirmTitle | 是否确定？ |
| etc菜单选项 | menuetPoptionApprove | 批准 |
|  | menueToptionDelete | 删除 |
|  | menueToptionEdit | 编辑 |
|  | menuetCopyFlag | 旗标 |
|  | menueToptionShare | Share |
|  | MenuetCodestedat | 发布于{date} |
|  | menuetCitle | 更多 |

## 主持人界面 {#section_o5f_dl4_xz}

可供用户验证的主持人界面使用字符串。

| Element | Key | 默认文本 |
|---|---|---|
| 来自更多菜单的确认消息 | 通知已批准 | 已批准 |
|  | notificationDeleted | 已删除 |
|  | NotificationFlaged | 已标记 |

## 错误 {#section_gtk_cl4_xz}

可用于一般错误消息的字符串。

| Element | Key | 默认文本 |
|---|---|---|
|  | ErrorConnection | 哦-哦。您似乎没有良好的连接。 |
|  | ErrorDuplicate | 我们也喜欢您的备注，但不能再发布两次。 |
|  | ErrorGeneral | 出现错误。请重试。 |
|  | ErrorServer | 我们的服务器出错。再次试用？ |

