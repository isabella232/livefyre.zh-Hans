---
description: 使用 .js implementation 属性来执行 Sidenotes.
seo-description: 使用 .js implementation 属性来执行 Sidenotes.
seo-title: Sitenes实施
solution: Experience Manager
title: Sitenes实施
uuid: a13852e-e2 b0-4a86-97cd-d08 ab5 e cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Sitenes实施{#sidenotes-implementation}

## 使用 .js implementation 属性来执行 Sidenotes

要执行此功能，请传递要覆盖到Javascript配置对象的字符串的一个-1对象映射。如果不提供字段，则将使用默认文本。

### 示例

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
