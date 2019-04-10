---
description: Livefyre使用PUSH界面发送有关用户权限更改的外部系统信息。
seo-description: Livefyre使用PUSH界面发送有关用户权限更改的外部系统信息。
seo-title: 向外部系统发布用户权限(可选)
solution: Experience Manager
title: 向外部系统发布用户权限(可选)
uuid: 9c18b20d-3b93-4666-b7 de-1ec60318 cf88
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 向外部系统发布用户权限(可选){#posting-user-permissions-to-external-systems-optional}

Livefyre使用PUSH界面发送有关用户权限更改的外部系统信息。

## Livefyre Studio中的用户类型

| 用户类型 | 描述 |
|--- |--- |
| 所有者 | 此用户是所有者，并且可以主持内容，并分配新的版主。 |
| admin | 此用户是主持人，可以审核内容。 |
| 成员 | 此用户已列入白名单。发布的内容不会传递垃圾邮件或亵渎过滤器，并且不需要在预先审核的流中批准。 |
| none | 此用户是标准用户，没有特殊权限。 |
| outcast | 此用户被禁止参与任何对话。 |

要将用户权限发布到外部系统，您必须注册接收POST请求的权限数据的URL。

例如：

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| 参数 | 描述 |
|--- |--- |
| noknName | 您的Livefyre提供了网络名称。 |
| token | 有效的系统令牌。 |
| url | 要注册的URL。 |

注册的URL应接受包含以下数据的POST作为内容类型：application/x-www-form-urlencoded.

| 参数 | 描述 |
|--- |--- |
| jid | 更改其所属关系的用户的JID。JID是表单 `user_id@network`的字符串。 |
| 从属关系 | 分配的权限名称，必须为以下内容之一： `{admin | member | none | outcast | owner}` |

有关更新用户所属关系的其他信息，请参阅 [添加用户从属API参考](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post)。
