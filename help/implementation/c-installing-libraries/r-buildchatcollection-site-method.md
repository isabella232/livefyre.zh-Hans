---
description: 返回实例化为聊天类型的Collection对象。从Collection对象运行create_ or_ update()以完成构建过程。
seo-description: 返回实例化为聊天类型的Collection对象。从Collection对象运行create_ or_ update()以完成构建过程。
seo-title: BuildChatchCollection站点方法
solution: Experience Manager
title: BuildChatchCollection站点方法
uuid: 39ee32d0-29c9-47a8-a458-a3 cf7 a96 db30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d

---


# BuildChatchCollection站点方法{#buildchatcollection-site-method}

返回实例化为聊天类型的Collection对象。从Collection对象运行create_ or_ update()以完成构建过程。

| 变量 | Type | 描述 |
|--- |--- |--- |
| title | 字符串 | 集合的标题。 |
| articleID | 字符串 | 您选择在站点内识别集合的唯一文章ID。 |
| url | 字符串 | 此集合的规范绝对URL。 |

## Java示例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## NodeJS示例 {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## PHP示例 {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Python示例 {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## 拼音示例 {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
