---
description: 自定义LivefyreSiten说明的文本字符串
seo-description: 自定义LivefyreSiten说明的文本字符串
seo-title: Sid表示文本字符串
solution: Experience Manager
title: Sid表示文本字符串
uuid: a3735237-e55 d-4bc0-b88 d-8a323980 ee09
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sid表示文本字符串{#sidenotes-text-strings}

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
|  | DateTimeMonthths | 数组。默认值=`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
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

