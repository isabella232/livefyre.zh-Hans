---
description: 使用功能API实现流程自动化
seo-description: 使用功能API实现流程自动化
seo-title: 功能API
title: 功能API
uuid: eac3a156-0b60-4ffa-8b6f-e451eb03da77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 功能API{#feature-apis}

使用功能API实现流程自动化

使用功能API自动处理内容的特色。 例如，在创建实时博客或评论应用程序时，为选定审查方发布的所有内容提供功能，以引导对话并在流中建立一致性。

Livefyre提供功能API和非功能API。

## 功能 {#section_jpw_nqw_xz}

**资源**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

输&#x200B;入所选审查方的用户令牌。

**发布数据**

```
{value: <number>} 
```

该值将用于对特色内容进行排序，从最大到最小（10将显示在特色内容列表中的1之前）。 此值默认为 **现在** （在纪元时间），因此特色注释通常排序最新到最旧。

**示例响应**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>数据字段尚未使用。

## 取消功能 {#section_knh_mqw_xz}

**资源**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

输入所选审查方的用户令牌。

**示例响应**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>数据字段尚未使用。

