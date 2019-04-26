---
description: 返回实例化为博客类型的Collection对象。从Collection对象运行create_ or_ update()以完成构建过程。
seo-description: 返回实例化为博客类型的Collection对象。从Collection对象运行create_ or_ update()以完成构建过程。
seo-title: BuildSocialCollection站点方法
solution: Experience Manager
title: BuildSocialCollection站点方法
uuid: 6a5ec6-bc32-467a-ea6-a57 c defe067
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# BuildSocialCollection站点方法{#buildblogcollection-site-method}

返回实例化为博客类型的Collection对象。从Collection对象运行create_ or_ update()以完成构建过程。

| 变量 | Type | 描述 |
|--- |--- |--- |
| title | 字符串 | 集合的标题。 |
| articleID | 字符串 | 您选择在站点内识别集合的唯一文章ID。 |
| url | 字符串 | 此集合的规范绝对URL。 |

## Java示例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildBlogCollection(title, articleId, url); 
```

## NodeJS示例 {#section_xkd_gds_rz}

```
var collection = site.buildBlogCollection(title, articleId, url); 
```

## PHP示例 {#section_ghf_gds_rz}

```
$collection = site->buildBlogCollection(title, articleId, url); 
```

## Python示例 {#section_dwg_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

## 拼音示例 {#section_enh_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

