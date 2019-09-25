---
description: 构建Ping for Pull响应，将更新的用户信息传输到Livefyre。
seo-description: 构建Ping for Pull响应，将更新的用户信息传输到Livefyre。
seo-title: 构建Ping以进行拉式响应
solution: Experience Manager
title: 构建Ping以进行拉式响应
uuid: f90871d5-601f-40dc-b3d2-ab78635e4a88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# 构建Ping以进行拉式响应{#build-the-ping-for-pull-response}

构建Ping for Pull响应，将更新的用户信息传输到Livefyre。

| 类型 | 属性 | 描述 |
|--- |--- |--- |
| 需要字 *符串* | ID | 个人资料系统中用户的用户ID。 这在您网络中的所有用户中必须是唯一的，并且绝不能更改。 |
| 需要字 *符串* | display_name | 用户的显示名称。 这将使用用户发布的Livefyre内容呈现。 |
| 对象 *可选，但建议* | name | 用于定义用户的格式化名、名、名、中名和姓的字符串。 |
| 字符串 *可选，但建议使用* | 电子邮件 | 用户的电子邮件地址。 用于发送电子邮件通知。 |
| 字符串 *可选，但建议使用* | image_url | 要显示给用户的头像的URL。 Livefyre会根据需要将上传的图像缩放为100×100、75×75或50×50像素。 为获得最佳效果，用户应上传100×100像素的方形图像。 要确保在Livefyre中更新头像图像，请修改每个图像更新的image_url，以便Ping for Pull检测到图像已更改。 例如，在文件名中附加时间戳或增加图像更改。 注意： 所有URL必须完全限定且可访问。 |
| 字符串 *可选，但建议使用* | profile_url | 指向您站点上用户的个人资料页面的URL。 |
| 字符串 *可选，但建议使用* | settings_url | 指向页面的URL，用户可在该页面中为您的站点配置用户的配置文件设置。 |
| 阵列 *可选，但建议* | 标记 | 用于将用户分配到用户组。 标记可能包括1-63个字母数字和下划线字符。 |
| Boolean可 *选，但建议* | autofollow_conversions | 定义用户是否希望在发布到集合后自动关注该集合。 当遵循集合时，用户在其他用户参与时会收到电子邮件通知。 可能为真或假。 默认值为true。 |
| 对象 *可选，但建议* | email_notifications | 定义可用Livefyre电子邮件通知的频率。 可以为每个通知类型设置不同的频率。 默认情况下，不会发送通知。 <br><ul><li> 在列出的活动后立即发出通知。 </li><li>通常会批量发送通知。 </li><li> 绝不会发送活动的电子邮件通知。 </li><li>*注释*:定义当其他用户将此用户正在关注的内容发布到集合时发送通知的时间。 </li><li>*回复*:定义当其他用户回复此用户的内容时发送通知的时间。</li><li>*喜欢*:定义当其他用户喜欢此用户的内容时发送通知的时间。</li><li>*drocidator_comments*:定义当用户将内容发布到网络中的任何集合时，通知发送给版主的时间。</li><li>*审查方_标志*:定义当其他用户标记网络中任何集合中的内容时通知发送给审核者的时间。</li></ul> |
| 字符串可 *选* | 位置 | 用户提交的位置。 |
| 字符串可 *选* | 生物 | 用户提交的自传。 |
| 阵列可 *选* | 网站 | 一组用户提交的站点。 最大= 2。 |
| 对象可 *选* | display_rules | 定义哪些配置文件属性对其他用户可公开查看。 每个可用参数都采用布尔输入true或false。 可用参数：  <br><ul><li>生物 </li><li> 位置</li><li>  性别 </li><li>nameimage </li><li> remote_profile_url</li></ul> |
| Boolean可 *选* | 主持人 | 定义用户是否具有跨网络的审查方权限。 |
| Boolean可 *选* | gravatar_disabled | 定义如果未提供image_url，是否禁用Livefyre对gravatar的使用。 |

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
