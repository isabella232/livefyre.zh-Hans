---
description: Livefyre使用PUSH界面发送有关用户权限更改的外部系统信息。
title: 将用户权限过帐到外部系统（可选）
exl-id: 335c9ff2-e392-4310-aad2-7890c8e82eba
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 4%

---

# 将用户权限过帐到外部系统（可选）{#posting-user-permissions-to-external-systems-optional}

Livefyre使用PUSH界面发送有关用户权限更改的外部系统信息。

## Livefyre Studio中的用户类型

| 用户类型 | 描述 |
|--- |--- |
| 所有者 | 此用户是所有者，可以审核内容并分配新的审核者。 |
| admin | 此用户是审查方，可以审核内容。 |
| 成员 | 此用户允许列出。 发布的内容不会通过垃圾邮件或污秽过滤器，并且在预先审核的流中不需要批准。 |
| 无 | 此用户是标准用户，没有特殊权限。 |
| outcast | 此用户已被禁止参与任何对话。 |

要将用户权限发布到外部系统，您必须注册一个URL，该URL接收权限数据作为POST请求。

例如：

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| 参数 | 描述 |
|--- |--- |
| networkName | 您的Livefyre提供的网络名称。 |
| 令牌 | 有效的系统令牌。 |
| url | 要注册的URL。 |

已注册的URL应接受以下数据的POST作为内容类型：application/x-www-form-urlencoded.

| 参数 | 描述 |
|--- |--- |
| jid | 其所属关系已更改的用户的JID。 JID是`user_id@network`形式的字符串。 |
| 从属关系 | 分配的权限的名称，必须为以下任一选项： `{admin | member | none | outcast | owner}` |

有关更新用户关联设置的详细信息，请参阅[添加用户关联API参考](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post)。
