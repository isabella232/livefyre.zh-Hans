---
description: 自定义Livefyre应用程序的字符串。
seo-description: 自定义Livefyre应用程序的字符串。
seo-title: 本地化字符串
solution: Experience Manager
title: 本地化字符串
uuid: c0ab352d-5d3a-45d7-bbd0-aed165835646
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '1996'
ht-degree: 8%

---


# 本地化字符串{#localize-strings}

自定义Livefyre应用程序的字符串。

可以自定义任何Livefyre应用程序中大多数HTML元素的文本字符串。 这样，可以灵活地将呈现的HTML元素（如“发布为”按钮、“注释计数”文本或“登录”按钮）的文本更改为任何有效的UTF-8字符串。 使用此功能为流实施添加个性化，或在应用程序中为用户群本地化语言。

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
   * [Sidesk](/help/using/c-settings-other/c-translation-sets/c-sidenotes-text-strings.md#c_sidenotes_text_strings)

## 实施 {#section_im4_224_xz}

要实现此功能，请传入要覆盖的字符串的1-1对象映射到JavaScript配置对象。 如果您不提供字段，则将使用默认文本。

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

本页列表了可能为Livefyre核心应用程序自定义的所有文本字符串。

## 帐户访问{#section_cm3_d24_xz}

可用于身份验证过程的字符串，以及来自已验证的用户菜单的字符串。

![](assets/strings_threadheader-150x40.png)

| 元素 | 键 | 默认文本 |
|---|---|---|
|  | displayName | %s |
|  | editProfile | 编辑用户档案 |
|  | notificationSettings | 通知设置 |
|  | siteAdmin | Admin Console（指向Studio的链接） |
|  | 注销 | 注销 |

## 流信息{#section_wx1_c24_xz}

可用于内容流信息和显示的字符串。 列表监听的人数、向应用程序发布的帖子数，并允许用户登录或访问其帐户信息。

| 键 | 默认文本 | 流数据 |
|---|---|---|
|  | commentCountLabelZero | %s注释 |
|  | commentCountLabel | %s注释 |
|  | commentCountLabelPlural | %s注释 |
|  | listenerCount | 倾听 |
|  | listenerCountPlural | 倾听 |
|  | liveblogPostCountLabelZero | 帖子 |
|  | liveblogPostCountLabel | 帖子 |
|  | liveblogPostCountLabelPlural | 个帖子 |
| 线程选项 | threadBreakoutButton | 显示整个线程 |
|  | 切换折叠 | 切换折叠 |
| 高速／排队注释 | 刷新 | 刷新 |
|  | newComment | 新建注释 |
|  | newComments | 新建注释 |
|  | newReply | 新回复 |
|  | newReplies | 新回复 |

## 流排序{#section_ih2_124_xz}

允许使用按年龄或人气对返回的内容进行排序。

![](assets/strings_newestoldesttop-1-150x56.png)

| 键 | 默认文本 | 标题选项 |
|---|---|---|
|  | sortNewbent | 最新 |
|  | sortLosted | 最旧 |
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

列表发布信息：用户名、所有已应用的用户标记和发布时间。

![](assets/strings_authorinfo-150x52.png)  ![](assets/strings_posttime-150x45.png)

| 键 | 默认文本 | 作者 |
|---|---|---|
|  | 主持人 | 主持人 |
|  | 悬浮卡视图配置文件 | 视图完整用户档案 |
| 发布信息 | timeJustNow | 刚才 |
|  | timeMinutesAgo | 分钟前 |
|  | timeMinutesAgoPlural | 分钟前 |
|  | timeHoursAgo | 小时前 |
|  | timeHoursAgoPlural | 小时前 |
|  | timeDaysAgo | 天前 |
|  | timeDaysAgoPlural | 天前 |
|  | likesPlural | 称赞次数 |
|  | likesSingular | 点赞 |
|  | 审查方编辑时间戳 | 主持人编辑 |
|  | commentTombstone | 此注释已被删除 |
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
| 编辑器按钮 | 跟 | + 关注 |
|  | 取消跟踪 | -取消关注 |
|  | liveblogFollow | 关注实时博客 |
|  | liveblogUnfollow | 取消关注实时博客 |
|  | postButton（可用于登录用户。） | 发布评论 |
|  | postAsButton（对未验证的用户可用。） | 将评论发布为…… |
|  | postEditButton | 编辑注释 |
|  | postEditAsButton | 将注释编辑为…… |
|  | postEditCancelButton | 取消 |
|  | editorDisabled | 此对话当前不会显示新评论。 |
| 聊天选项 | livechatPostButtonLabel | 帖子 |
|  | livechatPostEditButton | 编辑 |
|  | livechatWindowsInstruction | 按Ctrl+Enter可发布内容 |
|  | livechatOtherInstruction | 按command+enter可进行发布 |

## 响应选项{#section_zvt_qd4_xz}

除非另有说明，否则所有登录用户均可使用。 将鼠标悬停在内容面板上即可访问。

![](assets/strings_banusermodal-150x36.png)

| 键 | 默认文本 |  |
|---|---|---|
| 用户响应选项 | 面向最终用户。 |  |
| flagButton | 标记 |
|  | flagCommentTooltip | 标记 |
|  | editButton(仅适用于作者和版主（如果启用）。) | 编辑 |
|  | deleteButton(仅适用于作者和版主（如果启用）。) | 删除 |
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
| 标志模态 | flagTitle | 标记%s的注释 |
|  | flagSubtitle | 标记为 |
|  | flagDefaultSelectOption | 选择 |
|  | flagSpam | 垃圾信息 |
|  | flagSpamButton | 垃圾信息 |
|  | flagSpamCommentTooltip | 垃圾信息 |
|  | flagOffension | 进攻性 |
|  | flagOffensionButton | 进攻性 |
|  | flagOffensionCommentTooltip | 进攻性 |
|  | flagSover | 反对 |
|  | flagSoverButton | 反对 |
|  | flagSoverCommentTooltip | 反对 |
|  | flagOffTopic | 关闭主题 |
|  | flagOfftopicButton | 关闭主题 |
|  | flagOfftopicCommentTooltip | 关闭主题 |
|  | flagEmail | 电子邮件 |
|  | flagEmailPlaceholder | you@example.com |
|  | flagNotes | 注释 |
|  | flagNotesPlaceholder | 开始在这里输入…… |
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
|  | shareText | 我刚发布了评论。 看看！ |

![](assets/strings_sharemodal-150x59.png)

| 键 | 默认文本 |  |
|---|---|---|
| 回复模态 | postReplyAsButton | 将评论发布为…… |
|  | postReplyButton（可用于登录用户。） | 发布评论 |
|  | backToHotThreads | 返回热线程 |

![](assets/strings_backto-150x48.png)

| 键 | 默认文本 |  |
|---|---|---|
| Twitter @turite modal | 提及标题 | 共享提及 |
|  | 提及子标题Twitter | 将推文共享到： |
|  | 提及默认文本 | 我在Livefyre评论中提到过您！ |
|  | 提及确认按钮 | 确定 |
|  | 提及取消按钮 | 取消 |
|  | 提及错误一般 | 哎呀！ 出了什么问题！ Livefyre已收到警报。 |
|  | 提及错误无选定 | 必须至少启用一个提及。 |
|  | 提及菜单标题 | 去看看和提及你的朋友 |
|  | 提及TwitterConnect | 连接到Twitter |
|  | 提及TwitterFicking | 正在获取朋友…… |
|  | 提及成功消息 | 已成功发送提及。 |

![](assets/strings_sharemention-150x60.png)

| 键 | 默认文本 |  |
|---|---|---|
| 编辑模态 | 适用于Studio管理员、用户管理者或版主 |  |
| @(@tunited.) | &lt;/>（打开自定义HTML窗口。） |  |
|  | customHtmlDialogTitle（显示为模态的标题。） | 添加自定义HTML |

![](assets/strings_moderatoreditmodal-150x49.png)

| 键 | 默认文本 |  |
|---|---|---|
| 审查方响应选项 | 适用于Studio管理员、用户管理者或版主。 |  |
| pendingComment | pending |
|  | banUserButton | 禁止用户 |
|  | banUserTooltip | 禁止用户 |
|  | bozoButton | 博佐 |
|  | bozoComment工具提示 | 博佐 |
|  | featureButton | 功能 |
|  | featureComment工具提示 | 功能 |
|  | unfeatureButton | 取消功能 |
|  | featuredComment工具提示 | 取消功能 |

![](assets/strings_adminoptions-150x33.png)

| 键 | 默认文本 |  |
|---|---|---|
| 禁止用户模式 | 适用于Studio管理员、用户管理者或版主。 |  |
| banTitle | 禁止用户 |  |
|  | banConfirmation | 是否确实要禁止此用户？ |
|  | banConfirmButton | 确定 |
|  | banCancelButton | 取消 |

## 注释通知程序{#section_qqt_pd4_xz}

如果启用，则位于页面底部，可用于所有Livefyre对话应用程序。

![](assets/strings_notifier-150x112.png)

|  | 键 | 默认文本 |
|---|---|---|
| 通知程序标签 | 注释通知程序 | 新建注释 |
|  | commentNotifierPlural | 新建注释 |
|  | liveblog通知程序 | 新帖子 |
|  | liveblogNotifierPlural | 新帖子 |

## 错误消息 {#section_omz_jxn_xz}

可用于可自定义错误消息的字符串。

| 键 | 默认文本 |
|---|---|
| errorAuthError | 您无权对此对话发表评论 |
| errorCommentsNotAllowed | 此对话不允许添加评论 |
| errorDefault | 出现错误. 请重试。 |
| errorDuplicate | 尽管您很喜欢自己的评论，但您不能发布两次。 |
| errorEditDuplicate | 编辑注释时，必须更改注释正文。 |
| errorEditNotAllowed | 不允许您编辑此对话中的评论。 |
| errorEditTimeExceeded | 抱歉，您的注释编辑期已过。 |
| errorEmpty | 您似乎正在尝试发布空注释。 |
| errorExpired | 您的会话已过期。 请重新加载该页面。 |
| errorFlagNotSelected | 请选择标记类型。 |
| errorGuestLiked | 抱歉，只有那些有帐户的人才能喜欢内容。 |
| errorIndeficientPermissions | 权限不足 |
| errorInvalidChar | 您似乎在尝试发布无效字符。 |
| errorLikeOwnComment | 您不能喜欢自己的评论 |
| error格式错误 | 您似乎在尝试发布格式错误的内容。 |
| errorMaxChars | 抱歉，您的评论太长。 请编辑，然后重试。 |
| errorMediaNotAvailable | 媒体不再可见。 |
| errorShowMore | 加载更多注释时出错。 |
| MultipleMediaNotAllowedError | 您的权限一次只授予您一个媒体附件。 |

## 时间和日期格式{#section_yz4_g5n_xz}

翻译和自定义日期在可视化应用程序内内容卡上的显示方式。

| 键 | 默认文本 |
|---|---|
| 小时前 | {number}h |
| hoursAgoSingular | {number}h |
| 现在 | 1 |
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
| postButtonText | 您在想什么？ |
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

可用于Mosaics的字符串。

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

可用于上传应用程序的字符串。

| 键 | 默认文本 |
|---|---|
| postButtonText | 您在想什么？ |
| postModalTitle | 发布您的评论 |
| postModalButton | 发布您的评论 |
| postModalTitlePlaceholder | 输入标题 |
| postModalPlaceholder | 你想说什么？ |
| postModalConfirationTitle | 感谢您发帖！ |
| postModalConfirmationMessage | 您的帖子正在审核中。 |
| postModalConfirmationButton | 完成 |
| title |  |
| message |  |
| editorErrorAttachmentsRequired | 附件是必需的 |
| editorErrorBody | 请添加消息 |
| editorErrorDuplicate | 尽管您喜欢纸条，但您不能发布两次 |
| editorErrorGeneric | 出现错误 |
| editorErrorTitleRequired | 标题是必需的 |

## 投票 {#section_pdg_fwh_xz}

可用于投票的字符串。

| 键 | 默认文本 |
|---|---|
| totalPettionsLabel | %s总票数 |
| shareStringText | 我刚刚投了%s票，您投了什么票？ |
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
| emailWhenSomeReplies | 有人回复我时发送电子邮件 |
| emailCommentsIFollow | 在我关注的对话中通过电子邮件发送评论 |
| emailSenttoResetPassword | 电子邮件已发送！ 检查您的收件箱以获取重置密码的链接 |
| emailVerificationSent | 电子邮件验证已发送 |
| firstName | 名字 |
| forgotPassword | 忘记密码？ |
| forgotYourPassword | 忘记了密码？ |
| forgotYourPasswordInstructions | 请在下面输入您的用户名或电子邮件地址，我们会向您发送一个用于更改密码的链接。 |
| formInputCloseButtonText | Close |
| formInputCancelButtonText | 取消 |
| formInputSaveButtonText | 保存 |
| hasNotLeftAnyComments | 没有留下任何评论 |
| locationIsFrom | 来自 |
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
| 加载配置文件 | 加载用户档案 |
| newPassword | 新密码 |
| 旧密码 | 旧密码 |
| on | on |
| 或 | 或 |
| passwordLinkExpired | 您单击重置密码的链接已过期。 再次重置您的密码，我们将向您发送新链接。 |
| pleascheckEmailToComplete | 请检查您的电子邮件以完成注册。 |
| 已发布 | 已发布 |
| poweredBy | 由 |
| profileNotificationImmediate | immediate |
| profileNotificationHourly | 小时 |
| profileNotificationNever | never |
| recentComments | 近期评论 |
| 重置 | Reset |
| resetPassword | 重置密码 |
| 登录 | 登录 |
| signInWith | 使用 |
| signInWithEmail | 使用电子邮件登录 |
| 注册 | 注册 |
| socialAccount | 社交帐户 |
| successPasswordChanged | 成功! 您的密码已更改，您现在已登录 |
| termsAndConditions | 条款和条件 |
| termsAndConditionsIntro | 注册后，您接受 |
| termsOfUse | 使用条款 |
| termsOfUseIntro | 登录即表示您同意 |
| thisUser | 此用户 |
| verifyPassword | 验证密码 |
| fileSizeLimit | 最大2MB |
| 帐户未找到 | 找不到帐户 |
| avatarImageExceedSize | 您的头像图像已超过2mb文件限制 |
| fieldrequired | 字段仅接受整数 |
| fieldonlyacceptsaidemail | 字段仅接受有效的电子邮件 |
| fieldonlyacceptsletter | 字段仅接受字母 |
| filezemustbelessthanMB | 文件大小必须小于{#}MB |
| invalidusernamepassword | 用户名或密码无效 |
| 最小长度 | {#}字符的最小长度 |
| 最大长度字符 | 最大长度{#}个字符 |
| 错误 | 出现错误 |
| 此字段为必填 | 该字段为必填。 |
| 有效文件扩展 | 有效的文件扩展名 |
| 值自匹配 | 值必须匹配 |
| passwordLength | 长度为6到32个字符。 |
| passwordCharacters | 包括小写和大写字符。 |
| passwordSymbols | 至少包含一个数字和一个符号。 |
| passwordUsername | 不包含用户名。 |
| passwordPopover标题 | 您的密码需要： |
| passwordErrorContainsFirstName | 您输入的密码包含您的用户名、名或姓。 为安全起见，请输入不包含用户名、名或姓的密码。 另请记住，您的密码需要包含：6到32个字符大写字符A小写字符A符号 |
| passwordErrorContainsLastName | 您输入的密码包含您的用户名、名或姓。 为安全起见，请输入不包含用户名、名或姓的密码。 另请记住，您的密码需要包含：6到32个字符大写字符A小写字符A符号 |
| passwordErrorContainsUsername | 您输入的密码包含您的用户名、名或姓。 为安全起见，请输入不包含用户名、名或姓的密码。 另请记住，您的密码需要包含：6到32个字符大写字符A小写字符A符号 |
| passwordErrorTooShort | 密码字最少6个字符 |
| passwordErrorTooLong | 密码最多32个字符 |
| passwordErrorMissingUppercase | 密码至少应包含一个大写字符 |
| passwordErrorMissingLowercase | 密码至少应包含一个小写字符 |
| passwordErrorMissingSymbol | 密码集`!@#$%^&*()?.,<>\’;:”[]{}|`中至少应包含一个符号 |


