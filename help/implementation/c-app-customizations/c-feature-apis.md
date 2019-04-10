---
description: 使用功能API实现流程自动化
seo-description: 使用功能API实现流程自动化
seo-title: 功能API
title: 功能API
uuid: eac3a156-0b60-4ffa-8b6f-e451 eb03 da77
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 功能API{#feature-apis}

使用功能API实现流程自动化

使用功能API自动完成内容的特色。例如，创建Live Blog或评论App时，功能由选定主持人发布以指导对话，并在流中建立一致性。

Livefyre提供功能和Unfeature API。

## 功能 {#section_jpw_nqw_xz}

**资源**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

输入选定主持人的用户令牌。

**帖子数据**

```
{value: <number>} 
```

此值用于对特色内容进行排序，最大为最小(10将显示在特色内容列表中1)。此值默认为 **在Epoch** 时间，因此典型注释通常会被排序为最旧。

**示例响应**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>数据字段尚未使用。

## Unfeature {#section_knh_mqw_xz}

**资源**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

输入选定主持人的用户令牌。

**示例响应**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>数据字段尚未使用。

