---
description: 构建“提取”响应以将更新的用户信息传输到Livefyre。
seo-description: 构建“提取”响应以将更新的用户信息传输到Livefyre。
seo-title: 构建用于拉动响应的ping
solution: Experience Manager
title: 构建用于拉动响应的ping
uuid: f90871d5-601f-40dc-40 dc-b3 d2-ab78635 e4 a88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# 构建用于拉动响应的ping{#build-the-ping-for-pull-response}

构建“提取”响应以将更新的用户信息传输到Livefyre。

| Type | 属性 | 描述 |
|--- |--- |--- |
| String *required* | id | 配置文件系统中用户的用户ID。这在网络中的所有用户中必须是唯一的，并且绝不能更改。 |
| String *required* | display_ name | 用户的显示名称。此操作将使用用户发布的Livefyre内容进行渲染。 |
| 对象 *可选，但推荐* | name | 用于定义用户格式化的、第一个、中间和姓的字符串。 |
| 字符串 *可选，但建议使用* | email | 用户的电子邮件地址。用于发送电子邮件通知。 |
| 字符串 *可选，但建议使用* | image_ url | 要供用户显示的头像URL。根据需要，Livefyre将上传的图像缩放为100×100、75×75或50×50像素。为获得最佳效果，用户应上传方形图像，100×100像素。要确保在Livefyre中更新avar图像，请修改每个图像更新的image_ url，以便Ting for Draw检测图像是否已更改。例如，将时间戳附加到文件名，或增加图像的更改。注意：所有URL必须具有完全资格且可访问。 |
| 字符串 *可选，但建议使用* | profile_ url | 站点上用户配置文件页面的URL。 |
| 字符串 *可选，但建议使用* | settings_ url | 指向页面的URL，用户可在该页面上配置用户的个人资料设置。 |
| Array *可选，但推荐* | 标记 | 用于将用户分配给用户组。标记可能包括1-63字母数字和下划线字符。 |
| Boolean *可选，但建议使用* | autoollow_ convertly | 定义用户在发布到集合后是否希望自动跟随集合。在以下集合下，用户在其他用户参加时接收电子邮件通知。可能为true或false。默认为true。 |
| 对象 *可选，但推荐* | email_ notifications | 定义可用Livefyre电子邮件通知的频率。可以为每个通知类型设置不同频率。默认情况下，不会发送通知。 <br><ul><li> 立即在列出的活动后发出通知。 </li><li>通常会批量通知通知。 </li><li> 绝不会发送活动的电子邮件通知。 </li><li>*评论*：定义当其他用户将内容发布到此用户所关注集合时发送通知的时间。 </li><li>*回复*：定义当其他用户对此用户的内容进行回复时发送通知的时间。</li><li>*喜欢*：定义当其他用户喜欢此用户的内容时发送通知的时间。</li><li>*审核者_评论*：定义当用户将内容发布到网络中的任何集合时向审核者发送通知的时间。</li><li>*审核者_标记*：定义当其他用户在网络中的任何集合中标记内容时，将通知发送给审核者。</li></ul> |
| 字符串 *可选* | location | 用户提交的位置。 |
| 字符串 *可选* | 生物 | 用户提交的自动专区。 |
| Array *可选* | 网站 | 一组用户提交的站点。Max=2。 |
| 对象 *可选* | display_ rules | 定义其他用户公开可见的配置文件属性。每个可用参数都将Boolean输入true或false输入。可用参数： <br><ul><li>生物 </li><li> location</li><li>  性别 </li><li>nametimage </li><li> remote_ profile_ url</li></ul> |
| Boolean *可选* | 主持人 | 定义用户是否具有跨网络的主持人权限。 |
| Boolean *可选* | account_ disabled | 定义是否在未提供image_ url的情况下禁用Livefyre对区域符号的使用。 |

## 示例响应 {#section_uxt_3dd_mz}

```
{
 "id": "1234567890",
 "display_name": "Bob Dole",
 "name": {
   "formatted": "Bob Joseph Dole",
   "first": "Bob",
   "middle": "Joseph",
   "last": "Dole"
 },
   "email": "bob@dole.com",
   "image_url": "https://dole.com/images/bob.jpg",
   "profile_url": "https://site.com/bobdole",
   "settings_url":"https://site.com/settings",
   "tags": ["bob", "dole"],
   "autofollow_conversations": "true",
   "email_notifications": {
      "comments": "never",
      "replies": "immediately",
      "likes": "often",
      "moderator_comments": "immediately",
      "moderator_flags": "immediately" 
 },
  "location": "Washington D.C., USA",
  "bio": "Bob Dole speaks in the third person",
  "websites": ["https://dole.com/blog/", "https://bobdolerocks.com"],
  "display_rules": {
      "bio": "false",
      "location": "false",
      "gender": "false",
      "name": "false",
      "image": "false",
      "remote_profile_url": "false"
  },
  "moderator": "true",
  "gravatar_disabled": "false"
}
```
