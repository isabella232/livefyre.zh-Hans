---
description: 自定义Livefyre应用程序的字符串。
title: Localize Strings
exl-id: 5eb452e3-3b33-4861-9b62-5a41221defab
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1987'
ht-degree: 8%

---

# Localize Strings{#localize-strings}

自定义Livefyre应用程序的字符串。

可以自定义任何Livefyre应用程序中大多数HTML元素的文本字符串。 这样，可以灵活地将呈现的HTML元素（如“发布为”按钮、“注释计数”文本或“登录”按钮）的文本更改为任何有效的UTF-8字符串。 使用此功能为流的实施添加个性，或为用户在应用程序中本地化语言。

* 评论、聊天和实时博客

   * [实施](#c-localize-strings/section_im4_224_xz)
   * [帐户访问](#c-localize-strings/section_cm3_d24_xz)
   * [流信息](#c-localize-strings/section_wx1_c24_xz)
   * [流排序](#c-localize-strings/section_ih2_124_xz)
   * [内容信息](#c-localize-strings/section_llv_yd4_xz)
   * [特色内容](#c-localize-strings/section_gmw_vd4_xz)
   * [文本编辑器](#c-localize-strings/section_ky5_td4_xz)
   * [响应选项](#c-localize-strings/section_zvt_qd4_xz)
   * [注释通知程序](#c-localize-strings/section_qqt_pd4_xz)
   * [错误消息](#c-localize-strings/section_omz_jxn_xz)

* [时间和日期格式](#c-localize-strings/section_yz4_g5n_xz)
* [媒体墙](#c-localize-strings/section_vwt_d5n_xz)
* [地图](#c-localize-strings/section_fxv_c5n_xz)
* [马赛克](#c-localize-strings/section_e2s_b5n_xz)
* [轮播](#c-localize-strings/section_l2z_hkn_xz)
* [功能卡](#c-localize-strings/section_mw2_hkn_xz)
* [投票](#c-localize-strings/section_pdg_fwh_xz)
* [Livefyre Identity](#c-localize-strings/section_zc3_xvh_xz)
* 更多:
   * [审阅文本字符串](/help/using/c-settings-other/c-translation-sets/c-review-text-strings.md#c_review_text_strings)
   * [Siestr](/help/using/c-settings-other/c-translation-sets/c-sidenotes-text-strings.md#c_sidenotes_text_strings)

## 实施 {#section_im4_224_xz}

要实现此功能，请传递要覆盖的字符串的1-1对象映射到JavaScript配置对象。 如果您不提供字段，则将使用默认文本。

示例：

```
var customStrings = {     
   postAsButton: "New Post As Text",     
   postEditButton: "New Post Edit Text"  
};   
   convConfig["strings"] = customStrings; fyre.conv.load(     
   networkConfig,     
   [convConfig],     
   function(){}  
);
```

本页列表了可为Livefyre核心应用程序自定义的所有文本字符串。

## 帐户访问{#section_cm3_d24_xz}

可用于身份验证过程的字符串，以及已验证的用户菜单中的字符串。

![](assets/strings_threadheader-150x40.png)

| 元素 | 键 | 默认文本 |
|---|---|---|
|  | displayName | %s |
|  | editProfile | 编辑用户档案 |
|  | notificationSettings | 通知设置 |
|  | siteAdmin | Admin Console（指向Studio的链接） |
|  | 注销 | 注销 |

## 流信息{#section_wx1_c24_xz}

可用于内容流信息和显示的字符串。 列表侦听的人数、发布到应用程序的帖子数，并允许用户登录或访问其帐户信息。

| 键 | 默认文本 | 流数据 |
|---|---|---|
|  | commentCountLabelZero | %s注释 |
|  | commentCountLabel | %s注释 |
|  | commentCountLabelPlural | %s注释 |
|  | listenerCount | 监听 |
|  | listenerCountPlural | 倾听 |
|  | liveblogPostCountLabelZero | 帖子 |
|  | liveblogPostCountLabel | 帖子 |
|  | liveblogPostCountLabelPlural | 个帖子 |
| 线程选项 | threadBreakoutButton | 显示整个线程 |
|  | toggleCollapse | 切换折叠 |
| 高速/排队注释 | 刷新 | 刷新 |
|  | newComment | 新建注释 |
|  | newComments | 新建注释 |
|  | newReply | 新回复 |
|  | newReplies | 新回复 |

## 流排序{#section_ih2_124_xz}

允许用户按年龄或受欢迎程度对返回的内容进行排序。

![](assets/strings_newestoldesttop-1-150x56.png)

| 键 | 默认文本 | 标题选项 |
|---|---|---|
|  | sortNewst | 最新 |
|  | sortOlst | 最旧 |
|  | sortTopComments | 热门评论 |
|  | sortHotThreads | 热线程 |
|  | sortSeparator |  |  |
|  | streamSorting | 正在加载 |
|  | topCommentsContentNotFoundMsg | 还没有足够的赞。 |
|  | hotThreadsContentNotFoundMsg | 还没有足够的线程。 |
|  | streamRefreshMsg | 了解新增功能。 |
| 页脚选项 | archiveHeaderTitle | 从存档 |
|  | archiveShow更多 | 显示更多 |
|  | showMore | 显示更多注释 |
|  | showMoreLiveblog | 显示更多帖子 |

![](assets/strings_threadend-150x47.png)

## 内容信息{#section_llv_yd4_xz}

列表发布信息：用户名、任何已应用的用户标记和帖子时间。

![](assets/strings_authorinfo-150x52.png)  ![](assets/strings_posttime-150x45.png)

| 键 | 默认文本 | 作者 |
|---|---|---|
|  | 主持人 | 主持人 |
|  | slaffcardViewProfile | 视图完整用户档案 |
| 帖子信息 | timeJustNow | 刚才 |
|  | timeMinutesAgo | 分钟前 |
|  | timeMinutesAgoPlural | 分钟前 |
|  | timeHoursAgo | 小时前 |
|  | timeHoursAgoPlural | 小时前 |
|  | timeDaysAgo | 天前 |
|  | timeDaysAgoPlural | 天前 |
|  | likesPlural | 称赞次数 |
|  | likesSingular | 点赞 |
|  | 审查方编辑时间戳 | 主持人编辑 |
|  | commentTombstone | 此评论已被删除 |
|  | permalinkNotFoundMsg | 此注释不再可见。 |
|  | quickProfile工具提示 | 快速用户档案 |

## 特色内容{#section_gmw_vd4_xz}

如果启用，则特色内容将列在流的顶部。

|  | 键 | 默认文本 |
|---|---|---|
| 特色标签 |  |  |
| ![](assets/strings_featuredcontent-150x40.png) | featuredCommentsTag | 特色 |
|  | featuredCommentsTitlePlural | 特色评论 |

## 文本编辑器{#section_ky5_td4_xz}

默认情况下，位于页面顶部的所有用户均可使用。

![](assets/strings_texteditor-1-150x77.png)

|  | 键 | 默认文本 |
|---|---|---| 
| 编辑器按钮 | flow | + 关注 |
|  | unfollow |  — 取消关注 |
|  | liveblogFollow | 关注实时博客 |
|  | liveblogUnfollow | 取消关注实时博客 |
|  | postButton（可用于登录用户。） | 帖子评论 |
|  | postAsButton（对未验证的用户可用。） | 将评论发布为…… |
|  | postEditButton | 编辑注释 |
|  | postEditAsButton | 将注释编辑为…… |
|  | postEditCancelButton | 取消 |
|  | editorDisabled | 此对话当前已关闭，无需新评论。 |
| 聊天选项 | livechatPostButtonLabel | 帖子 |
|  | livechatPostEditButton | 编辑 |
|  | livechatWindowsInstruction | 按Ctrl+Enter可发布 |
|  | livechatOtherInstruction | 按command+enter可发布 |

## 响应选项{#section_zvt_qd4_xz}

除非另行说明，否则可供所有登录用户使用。 将鼠标悬停在要访问的内容面板上。

![](assets/strings_banusermodal-150x36.png)

| 键 | 默认文本 |  |
|---|---|---|
| 用户响应选项 | 面向最终用户。 |  |
| flagButton | 标记 |
|  | flagCommentTooltip | 标记 |
|  | editButton（如果启用，则仅适用于作者和版主。） | 编辑 |
|  | deleteButton（如果启用，则仅适用于作者和版主。） | 删除 |
|  | deleteCommentTooltip | 删除 |
|  | shareButton | 共享 |
|  | shareCommentTooltip | 共享 |
|  | likeButton | 点赞 |
|  | 不同于按钮 | 取消称赞 |
|  | replyButton | 回复 |
|  | replyButtonSingular（可用于聊天和实时博客。） | 回复 |
|  | replyButtonPlural（可用于聊天和实时博客。） | 回复次数 |

![](assets/strings_responseoptions-150x35.png)

| 键 | 默认文本 |  |
|---|---|---|
| 标志模式 | flagTitle | 标记%s的注释 |
|  | flagSubtitle | 标记为 |
|  | flagDefaultSelectOption | 选择 |
|  | flagSpam | 垃圾信息 |
|  | flagSpamButton | 垃圾信息 |
|  | flagSpamCommentTooltip | 垃圾信息 |
|  | flagOffensive | 进攻 |
|  | flagOffensionButton | 进攻 |
|  | flagOffensionCommentTooltip | 进攻 |
|  | flagSarove | 反对 |
|  | flagSparokeButton | 反对 |
|  | flagScoverCommentTooltip | 反对 |
|  | flagOffTopic | 关闭主题 |
|  | flagOfftopicButton | 关闭主题 |
|  | flagOfftopicCommentTooltip | 关闭主题 |
|  | flagEmail | 电子邮件 |
|  | flagEmailPlaceholder | you@example.com |
|  | flagNotes | 注释 |
|  | flagNotesPlaceholder | 开始在此处键入…… |
|  | flagConfirmButton | OK |
|  | flagCancelButton | 取消 |
|  | flagConfirmationMessage | 是否将%s注释标记为%s? |
|  | flagSuccessMsg | 已标记评论。 |

![](assets/strings_flagmodal-150x87.png)

| 键 | 默认文本 |  |
|---|---|---|
| 共享模式 | shareTitle | 共享注释 |
|  | sharePlaceholderText | 你觉得呢？ |
|  | shareLabel | 分享于： |
|  | shareTextTwitter | 空 |
|  | shareTextFacebook | 空 |
|  | shareTextLinkedin | 空 |
|  | shareButtonText | 共享 |
|  | sharePermalink | 佩马林克 |
|  | loadingPermalink | 正在加载短url... |
|  | shareText | 我刚发了条评论。 看看！ |

![](assets/strings_sharemodal-150x59.png)

| 键 | 默认文本 |  |
|---|---|---|
| 回复模态 | postReplyAsButton | 将评论发布为…… |
|  | postReplyButton（可用于登录用户。） | 帖子评论 |
|  | backToHotThreads | 返回热线程 |

![](assets/strings_backto-150x48.png)

| 键 | 默认文本 |  |
|---|---|---|
| Twitter @mention modal | tuniteTitle | 分享提及 |
|  | tuniteSubtitleTwitter | 将推文共享到： |
|  | untiteDefaultText | 我在Livefyre评论中提到过你！ |
|  | untiteConfirmButton | 确定 |
|  | untiteCancelButton | 取消 |
|  | tuniteErrorGeneral | 糟糕！ 出了点问题！ Livefyre已收到警报。 |
|  | untiteErrorNoneSelected | 您必须至少启用一个提及。 |
|  | untiteMenuTitle | 去看你的朋友 |
|  | 提及TwitterConnect | 连接到Twitter |
|  | 提及TwitterFeiding | 正在获取朋友…… |
|  | tuniteSuccessMsg | 已成功发送提及。 |

![](assets/strings_sharemention-150x60.png)

| 键 | 默认文本 |  |
|---|---|---|
| 编辑模态 | 适用于Studio管理员、用户管理者或版主 |  |
| @(@mention.) | &lt;/>（打开自定义html窗口。） |  |
|  | customHtmlDialogTitle（显示为模态的标题。） | 添加自定义HTML |

![](assets/strings_moderatoreditmodal-150x49.png)

| 键 | 默认文本 |  |
|---|---|---|
| 审查方答复选项 | 适用于Studio管理员、用户管理者或版主。 |  |
| pendingComment | pending |
|  | banUserButton | 禁止用户 |
|  | banUserTooltip | 禁止用户 |
|  | bozoButton | 博佐 |
|  | bozoCommentTooltip | 博佐 |
|  | featureButton | 功能 |
|  | featureCommentTooltip | 功能 |
|  | unfeatureButton | 取消功能 |
|  | featuredCommentTooltip | 取消功能 |

![](assets/strings_adminoptions-150x33.png)

| 键 | 默认文本 |  |
|---|---|---|
| 禁止用户模式 | 适用于Studio管理员、用户管理者或版主。 |  |
| banTitle | 禁止用户 |  |
|  | banConfirmation | 是否确实要禁止此用户？ |
|  | banConfirmButton | 确定 |
|  | banCancelButton | 取消 |

## 通知程序{#section_qqt_pd4_xz}

如果已启用，则位于页面底部的所有Livefyre对话应用程序。

![](assets/strings_notifier-150x112.png)

|  | 键 | 默认文本 |
|---|---|---|
| 通知程序标签 | commentNotifier | 新建注释 |
|  | commentNotifierPlural | 新建注释 |
|  | liveblogNotifier | 新帖子 |
|  | liveblogNotifierPlural | 新帖子 |

## 错误消息 {#section_omz_jxn_xz}

可用于可自定义错误消息的字符串。

| 键 | 默认文本 |
|---|---|
| errorAuthError | 您无权对此对话发表评论 |
| errorCommentsNotAllowed | 此对话中不允许有评论 |
| errorDefault | 出现错误. 请重试。 |
| errorDuplicate | 尽管你很喜欢你的评论，但你不能发布两次。 |
| errorEditDuplicate | 编辑注释时，必须更改注释正文。 |
| errorEditNotAllowed | 不允许您编辑此对话的评论。 |
| errorEditTimeExceeded | 抱歉，您的注释编辑期已过。 |
| errorEmpty | 你似乎在尝试发布空评论。 |
| errorExpired | 您的会话已过期。 请重新加载该页面。 |
| errorFlagNotSelected | 请选择标志类型。 |
| errorGuestLiked | 抱歉，只有那些有帐户的人才能喜欢内容。 |
| errorIndeficedPermissions | 权限不足 |
| errorInvalidChar | 您似乎在尝试发布无效字符。 |
| errorLikeOwnComment | 您不能喜欢自己的评论 |
| errorFormable | 您似乎在尝试发布格式错误的内容。 |
| errorMaxChars | 抱歉，您的评论太长。 请编辑并重试。 |
| errorMediaNotAvailable | 媒体不再可见。 |
| errorShowMore | 加载更多注释时出错。 |
| MultipleMediaNotAllowedError | 您的权限一次只授予您一个媒体附件。 |

## 时间和日期格式{#section_yz4_g5n_xz}

翻译和自定义日期在可视化应用程序内内容卡上的显示方式。

| 键 | 默认文本 |
|---|---|
| hoursAgo | {number}h |
| hoursAgoSingular | {number}h |
| justNow | 1 |
| minutesAgo | {number}m |
| minutesAgoSingular | {number}m |
| monthDayFormat | {day} {monthAbbrev} |
| monthDayYearFormat | {day} {monthAbbrev} {year} |
| monthNames | 一月、二月、三月、四月、五月、六月、七月、八月、九月、十月、十一月、十二月 |
| monthNamesAbbrev | 1月、2月、3月、4月、5月、6月、7月、8月、9月、10月、11月、12月 |
| secondsAgo | {number}s |
| secondsAgoSingular | {number}s |

## 介质墙{#section_vwt_d5n_xz}

可用于媒体墙应用程序的字符串。

| 键 | 默认文本 |
|---|---|
| featuredText | 特色 |
| shareButtonText | 共享 |

| 键 | 默认文本 |
|---|---|
| postButtonText | 你在想什么？ |
| postModalTitle | 发布您的评论 |
| postModalButton | 发布您的评论 |
| postModalPlaceholder | 你想说什么？ |
| showMoreButtonText | 加载更多 |
| shareButtonText | 共享 |

## 地图 {#section_fxv_c5n_xz}

可用于映射的字符串。

| 键 | 默认文本 |
|---|---|
| featuredText | 特色 |
| shareButtonText | 共享 |

## 马赛克{#section_e2s_b5n_xz}

可用于Mosaic的字符串。

| 键 | 默认文本 |
|---|---|
| featuredText | 特色 |
| shareButtonText | 共享 |

## 轮播{#section_l2z_hkn_xz}

可用于传送的字符串。

| 键 | 默认文本 |
|---|---|
| featuredText | 特色 |
| shareButtonText | 共享 |

## 功能卡{#section_mw2_hkn_xz}

功能卡可用的字符串。

| 键 | 默认文本 |
|---|---|
| featuredText | 特色 |
| shareButtonText | 共享 |

## 上传应用程序{#section_grc_gkn_xz}

可用于上载应用程序的字符串。

| 键 | 默认文本 |
|---|---|
| postButtonText | 你在想什么？ |
| postModalTitle | 发布您的评论 |
| postModalButton | 发布您的评论 |
| postModalTitlePlaceholder | 输入标题 |
| postModalPlaceholder | 你想说什么？ |
| postModalConfirationTitle | 感谢您发帖！ |
| postModalConfirmationMessage | 您的帖子正在审核中。 |
| postModalConfirmationButton | 完成 |
| title |  |
| message |  |
| editorErrorAttachmentsRequired | 附件为必填项 |
| editorErrorBody | 请添加消息 |
| editorErrorDuplicate | 尽管你喜欢便条，但你不能发布两次 |
| editorErrorGeneric | 出错 |
| editorErrorTitleRequired | 标题是必填项 |

## 投票 {#section_pdg_fwh_xz}

可用于投票的字符串。

| 键 | 默认文本 |
|---|---|
| totalPettionsLabel | %s总票数 |
| shareStringText | 我刚刚投了%s票，你投了什么票？ |
| pollClosedLabel | 此投票当前已关闭 |

## Livefyre Identity {#section_zc3_xvh_xz}

可用于Livefyre Identity的字符串。

| 键 | 默认文本 |
|--- |--- |
| automaticallyFollowConversations | 自动关注我加入的对话 |
| back | 返回 |
| 生物 | 个人简介 |
| create | 创建 |
| createANewAccount | 创建新帐户 |
| createNewAccountWithEmail | 使用电子邮件创建新帐户 |
| changeAvatar | 更改头像 |
| chooseFile | 选择文件 |
| completeAccount | 完整帐户 |
| emailWhenSomeReplies | 当有人回复我 |
| emailCommentsIFollow | 在我关注的对话中通过电子邮件发送评论 |
| emailSenttoResetPassword | 电子邮件已发送！ 检查您的收件箱以查找重置密码的链接 |
| emailVerificationSent | 电子邮件验证已发送 |
| firstName | 名字 |
| forgotPassword | 忘记密码？ |
| forgotYourPassword | 忘记了密码？ |
| forgotYourPasswordInstructions | 请在下面输入您的用户名或电子邮件地址，我们将向您发送更改密码的链接。 |
| formInputCloseButtonText | Close |
| formInputCancelButtonText | 取消 |
| formInputSaveButtonText | 保存 |
| hasNotLeftAnyComments | 没有留下任何评论 |
| locationIsFrom | 的 |
| labelAvatar | 阿凡达 |
| labelComments | 注释 |
| labelConfirmNewPassword | 确认新密码 |
| labelConfirmPassword | 确认密码 |
| labelEmail | Email Address |
| labelLikes | 称赞次数 |
| labelLoading | 正在加载 |
| labelNewPassword | 新密码 |
| labelNotification | 通知 |
| labelPassword | 密码 |
| labelProfile | Profile |
| labelUsername | 用户名 |
| labelUsernameOrEmail | 用户名或电子邮件 |
| lastName | 姓氏 |
| livefyre帐户 | Livefyre帐户 |
| 位置 | 位置 |
| loadingProfile | 正在加载用户档案 |
| newPassword | 新密码 |
| oldPassword | 旧密码 |
| on | on |
| 或 | 或 |
| passwordLinkExpired | 您单击重置密码的链接已过期。 再次重置您的密码，我们将向您发送新链接。 |
| pleasecheckEmailToComplete | 请检查您的电子邮件以完成注册。 |
| 已发布 | 已发布 |
| poweredBy | 由 |
| profileNotificationImmediate | immediate |
| profileNotificationHourly | 每小时 |
| profileNotificationNever | never |
| recentComments | 最近的评论 |
| 重置 | Reset |
| resetPassword | 重置密码 |
| 登录 | 登录 |
| signInWith | 登录方式 |
| signInWithEmail | 使用电子邮件登录 |
| 注册 | 注册 |
| socialAccount | 社交帐户 |
| successPasswordChanged | 成功! 您的密码已更改，您现在已登录 |
| termsAndConditions | 条款和条件 |
| termsAndConditionsIntro | 注册即表示您接受 |
| termsOfUse | 使用条款 |
| termsOfUseIntro | 登录即表示您同意 |
| thisUser | 此用户 |
| verifyPassword | 验证密码 |
| fileSizeLimit | 最大2MB |
| 帐户未找到 | 找不到帐户 |
| avatarImageExceedSize | 您的头像图像已超过2mb文件限制 |
| field | 字段仅接受整数 |
| fieldonlyacceptsavidemail | 字段仅接受有效的电子邮件 |
| fieldonlyacceptsletter | 字段仅接受字母 |
| filesizemustbelessthanMB | 文件大小必须小于{#}MB |
| invalidusernameorpassword | 用户名或密码无效 |
| 最小长度字符 | {#}个字符的最小长度 |
| 最大长度字符 | 最大长度{#}个字符 |
| therewaserror | 出错 |
| 此字段为必填 | 该字段为必填。 |
| 有效的文件扩展 | 有效的文件扩展名 |
| 值自匹配 | 值必须匹配 |
| passwordLength | 长度为6到32个字符。 |
| passwordCharacters | 包括小写和大写字符。 |
| passwordSymbols | 至少包含一个数字和一个符号。 |
| passwordUsername | 不包含您的用户名。 |
| passwordPopoverTitle | 您的密码需要： |
| passwordErrorContainsFirstName | 您输入的密码包含您的用户名、名或姓。 出于安全原因，请输入不包含您的用户名、名或姓的密码。 另请记住，您的密码需要包含：6到32个字符大写字符A小写字符A符号 |
| passwordErrorContainsLastName | 您输入的密码包含您的用户名、名或姓。 出于安全原因，请输入不包含您的用户名、名或姓的密码。 另请记住，您的密码需要包含：6到32个字符大写字符A小写字符A符号 |
| passwordErrorContainsUsername | 您输入的密码包含您的用户名、名或姓。 出于安全原因，请输入不包含您的用户名、名或姓的密码。 另请记住，您的密码需要包含：6到32个字符大写字符A小写字符A符号 |
| passwordErrorTooShort | 密码至少6个字符 |
| passwordErrorTooLong | 密码最多32个字符 |
| passwordErrorMissingUpperase | 密码应至少包含一个大写字符 |
| passwordErrorMissingLowercase | 密码应至少包含一个小写字符 |
| passwordErrorMissingSymbol | 密码集`!@#$%^&*()?.,<>\’;:”[]{}|`中应至少包含一个符号 |
