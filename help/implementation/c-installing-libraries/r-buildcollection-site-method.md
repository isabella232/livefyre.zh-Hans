---
description: 'null'
seo-description: 'null'
seo-title: buildCollection站点方法
solution: Experience Manager
title: buildCollection站点方法
uuid: 52abc42a-9506-4492-b219-f2e05eb79c5f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 17%

---


# buildCollection Site Method{#buildcollection-site-method}

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| type | CollectionType | 集合的类型。 |
| title | 字符串 | 集合的标题。 |
| 文章Id | 字符串 | 您选择在您的站点中标识集合的唯一文章ID。 |
| url | 字符串 | 此集合的规范绝对URL。 |

## Java示例{#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## NodeJS示例{#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## PHP示例{#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Python示例{#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Ruby示例{#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
