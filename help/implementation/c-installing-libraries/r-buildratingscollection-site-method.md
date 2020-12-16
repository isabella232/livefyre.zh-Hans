---
description: 返回实例化为评级类型的Collection对象。 从Collection对象运行create_or_update()以完成构建过程。
seo-description: 返回实例化为评级类型的Collection对象。 从Collection对象运行create_or_update()以完成构建过程。
seo-title: buildRatingsCollection站点方法
title: buildRatingsCollection站点方法
uuid: 5eea2ba3-48e1-4cd2-aa73-ea81788af1df
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 6%

---


# buildRatingsCollection站点方法{#buildratingscollection-site-method}

返回实例化为评级类型的Collection对象。 从Collection对象运行create_or_update()以完成构建过程。

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| title | 字符串 | 集合的标题。 |
| 文章Id | 字符串 | 您选择在您的站点中标识集合的唯一文章ID。 |
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

