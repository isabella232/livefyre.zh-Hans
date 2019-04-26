---
description: null
seo-description: null
seo-title: Sid表示自定义字符串
title: Sid表示自定义字符串
uuid: 73745273-d3 fb-4556-8910-d147 fb37 a7 b4
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Sid表示自定义字符串{#sidenotes-custom-strings}

自定义字符串通过插入到SiteNote构造函数中的对象进行应用，并覆盖通过应用程序使用的默认字符串。这些内容可用于自定义语言的任何部分，以符合您的风格或语言规范。字符串将自动与默认值合并。

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| Key | 默认值 |
|---|---|
| appName | Siten表示 |
| CommentModeratorTag | Mod |
| 注释标记 | 待定 |
| 注释自述链接 | 阅读更多 |
| 注释链接 | 请参阅{number}回复 |
| 注释链接 | 请参阅回复 |
| CommentVoeCount | 投票 |
| 注释技术 | 投票 |
| editorPlaceHolder | 您想什么？ |
| editorPostBtn | 发布站点 |
| EditorPostBtnsMobile | Post |
| 编辑窗格 | 发布… |
| editorReplicBtn | 回复回复 |
| editorReplicitTitle | 回复回复 |
| 编辑标题 | Write Note |
| emptyImageBlockxt | 您想什么？ |
| emptyTextBlockXT | + |
| ErrorConnection | 哦-哦。您似乎没有良好的连接。 |
| ErrorDuplicate | 我们也喜欢您的备注，但不能再发布两次。 |
| ErrorGeneral | 出现错误。请重试。 |
| ErrorServer | 我们的服务器出错。再次试用？ |
| FacebookShareCaption | SiteNote on“{title}” |
| MenuAuthesignMsg | 您必须登录{action} |
| menuAuthSignInBtn | 登录 |
| menuBackBtn | 返回次数 |
| menuConfirmAc接受 | 是，{action} |
| menuConfirmCancel | 取消 |
| menuConfirmTitle | 是否确定？ |
| menuetPoptionApprove | 批准 |
| menueToptionDelete | 删除 |
| menueToptionEdit | 编辑 |
| menuetCopyFlag | 旗标 |
| menueToptionShare | Share |
| MenuetCodestedat | 发布于{date} |
| menuetCitle | 更多 |
| 菜单标记反对 | 反对 |
| MenuFlagoptionOfficy | 攻击性 |
| menuFlagoptionOffTopic | 关闭主题 |
| MenuFlagoptionSpam | 垃圾信息 |
| menuFlagtitle | 标记为… |
| menuInFocoCopyright | © Livefyre，Inc2014 |
| menuInfoHelp | 帮助 |
| menuInfolveFileLink | 访问Livefyre.com |
| menuRepliciesView回复 | 回复对话 |
| menuRepliciesViewTitle | 详细信息 |
| MenuShareOptionFacebook | Facebook |
| menuShareOptionLink | 复制Permalink |
| menuShareoptionLinkComplete | 已复制 |
| menushareoptionLinkFailed | 复制失败 |
| MenuShareOptionTwitter | Twitter |
| MenuShareTitle | Share |
| 通知已批准 | 已批准 |
| notificationDeleted | 已删除 |
| NotificationFlaged | 已标记 |
| permalinkBackBtn | 全部 |
| PermalinkTitle | Permalink |
| 问题解释 | 您现在可以直接在句子、段落、图像和引号上阅读和编写注释。<br><br>高亮显示文本并单击“fycon-write”图标，或单击每个段落末尾的“fycon-action-view”图标。 |
| 问题模型 | “熟悉的知识”是不正确的，只是因为它是“熟悉”的原因。 |
| 问题标题 | 什么是Sitenote？ |
| QueedCommentSocial | {number} New Sitenes |
| QueedCommentsSuble | 全新SitenOte |
| QueedDeployeesMultiple | {number}新回复 |
| QueedDeployeesingRumular | 个新回复 |
| replicyBtn | Reply |
| SignInPost | 登录以写入Sitenote |
| 幻灯片评论 | of |
| SliderInviteRead | 阅读阅读 |
| SliderInviteWrite | Write |
| sliderWriteText | 您想什么？点击以写入 |
| searchCollapseBtn | 折叠 |
| threadAxpandBtnMultiple | 展开{number}回复 |
| threadExpandBtn | 展开回复 |
| searchReplicBtn | 回复对话 |
