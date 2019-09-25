---
description: 返回实例化为“注释”类型的Collection对象。 从Collection对象运行createOrUpdate()以完成构建过程。
seo-description: 返回实例化为“注释”类型的Collection对象。 从Collection对象运行createOrUpdate()以完成构建过程。
seo-title: buildCommentsCollection站点方法
solution: Experience Manager
title: buildCommentsCollection站点方法
uuid: 0e5c062e-960d-4ab0-ba32-0965731a1571
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildCommentsCollection站点方法{#buildcommentscollection-site-method}

返回实例化为“注释”类型的Collection对象。 从Collection对象运行createOrUpdate()以完成构建过程。

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| title | 字符串 | 集合的标题。 |
| articleId | 字符串 | 您选择的唯一文章ID，用于标识站点中的集合。 |
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

## Ruby示例 {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
