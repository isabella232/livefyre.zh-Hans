---
title: buildCollection网站方法
description: buildCollection网站方法
exl-id: d5c9a2fb-2d30-44f4-8ebf-24b0ec7babee
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 15%

---

# buildCollection Site Method{#buildcollection-site-method}

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| type | CollectionType | 集合的类型。 |
| title | 字符串 | 集合的标题。 |
| articleId | 字符串 | 您选择的唯一文章ID，用于标识您网站中的集合。 |
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
