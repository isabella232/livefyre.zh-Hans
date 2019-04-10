---
description: 返回实例化为评级类型的Collection对象。从Collection对象运行create_ or_ update()以完成构建过程。
seo-description: 返回实例化为评级类型的Collection对象。从Collection对象运行create_ or_ update()以完成构建过程。
seo-title: BuildRatingSollection站点方法
title: BuildRatingSollection站点方法
uuid: 5eea2ba3-48e1-4cd2-aa73-ea81788 af1 df
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# BuildRatingSollection站点方法{#buildratingscollection-site-method}

返回实例化为评级类型的Collection对象。从Collection对象运行create_ or_ update()以完成构建过程。

| 变量 | Type | 描述 |
|--- |--- |--- |
| title | 字符串 | 集合的标题。 |
| articleID | 字符串 | 您选择在站点内识别集合的唯一文章ID。 |
| url | 字符串 | 此集合的规范绝对URL。 |

## Java示例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildRatingsCollection(title, articleId, url); 
```

## NodeJS示例 {#section_xkd_gds_rz}

```
var collection = site.buildRatingsCollection(title, articleId, url); 
```

## PHP示例 {#section_ghf_gds_rz}

```
$collection = site->buildRatingsCollection(title, articleId, url); 
```

## Python示例 {#section_dwg_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

## 拼音示例 {#section_enh_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

