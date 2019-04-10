---
description: 返回实例化为评论类型的Collection对象。从Collection对象运行createOrUpdate()以完成构建过程。
seo-description: 返回实例化为评论类型的Collection对象。从Collection对象运行createOrUpdate()以完成构建过程。
seo-title: BuildCommentsCollection站点方法
solution: Experience Manager
title: BuildCommentsCollection站点方法
uuid: 0e5c062e-960d-4ab0-ba32-0965731a1571
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# BuildCommentsCollection站点方法{#buildcommentscollection-site-method}

返回实例化为评论类型的Collection对象。从Collection对象运行createOrUpdate()以完成构建过程。

| 变量 | Type | 描述 |
|--- |--- |--- |
| title | 字符串 | 集合的标题。 |
| articleID | 字符串 | 您选择在站点内识别集合的唯一文章ID。 |
| url | 字符串 | 此集合的规范绝对URL。 |

## Java示例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## NodeJS示例 {#section_xkd_gds_rz}

```
var collection = site.buildCommentsCollection(title, articleId, url); 
```

## PHP示例 {#section_ghf_gds_rz}

```
$collection = site->buildCommentsCollection(title, articleId, url); 
```

## Python示例 {#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## 拼音示例 {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
