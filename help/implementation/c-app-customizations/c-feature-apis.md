---
description: 使用功能API实现流程自动化
seo-description: 使用功能API实现流程自动化
seo-title: 功能API
title: 功能API
uuid: eac3a156-0b60-4ffa-8b6f-e451eb03da77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---


# 功能API{#feature-apis}

使用功能API实现流程自动化

使用功能API自动执行内容特色化过程。 例如，在创建实时博客或评论应用程序时，请对选定审查方发布的所有内容进行功能设置，以指导对话并在流中建立一致性。

Livefyre优惠功能API和非功能API。

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

该值将用于对特色内容进行排序，从大到小(10将在特色内容列表显示在1之前)。 此值默认为大纪元时间的&#x200B;**now**，因此，特色注释通常会从最新到最旧排序。

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

输入所选审查方的用户令牌。

**示例响应**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>数据字段尚未使用。

