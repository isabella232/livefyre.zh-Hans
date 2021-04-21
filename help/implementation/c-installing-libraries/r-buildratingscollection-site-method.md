---
description: 返回实例化为评级类型的Collection对象。 从Collection对象运行create_or_update()以完成构建过程。
title: buildRatingsCollection网站方法
exl-id: 84af3bb2-95f0-40e0-9a4e-830772a71862
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 8%

---

# buildRatingsCollection网站方法{#buildratingscollection-site-method}

返回实例化为评级类型的Collection对象。 从Collection对象运行create_or_update()以完成构建过程。

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| title | 字符串 | 集合的标题。 |
| articleId | 字符串 | 您选择的唯一文章ID，用于标识您网站中的集合。 |
| url | 字符串 | 此集合的规范绝对URL。 |

## Java示例{#section_nyl_ycs_rz}

```
Collection collection = site.buildRatingsCollection(title, articleId, url); 
```

## NodeJS示例{#section_xkd_gds_rz}

```
var collection = site.buildRatingsCollection(title, articleId, url); 
```

## PHP示例{#section_ghf_gds_rz}

```
$collection = site->buildRatingsCollection(title, articleId, url); 
```

## Python示例{#section_dwg_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

## Ruby示例{#section_enh_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```
