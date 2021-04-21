---
description: 使用功能API实现流程自动化
title: 功能API
exl-id: 765e47fe-a406-44e6-b4fb-b2e85fc83c01
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# 功能API{#feature-apis}

使用功能API实现流程自动化

使用功能API自动处理特色内容的流程。 例如，在创建实时博客或评论应用程序时，请对选定审查方发布的所有内容进行功能设置，以引导对话并在流内建立一致性。

Livefyre可优惠功能API和未功能API。

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

该值将用于对特色内容进行排序，从大到小(在特色内容列表中，10显示在1之前)。 此值默认为大纪元时间的&#x200B;**now**，因此，特色注释通常将最新到最旧。

**示例响应**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>数据字段尚未使用。

## 取消功能{#section_knh_mqw_xz}

**资源**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

输入所选主持人的用户令牌。

**示例响应**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>数据字段尚未使用。
