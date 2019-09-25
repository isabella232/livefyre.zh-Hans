---
description: 使用 .js implementation 属性来执行 Sidenotes.
seo-description: 使用 .js implementation 属性来执行 Sidenotes.
seo-title: Sides Implementation
solution: Experience Manager
title: Sides Implementation
uuid: aa13852e-e2b0-4a86-97cd-d08ab5e2cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Sides Implementation{#sidenotes-implementation}

## 使用 .js implementation 属性来执行 Sidenotes

要实现此功能，请传递要覆盖的字符串的1-1对象映射到Javascript配置对象。 如果不提供字段，则将使用默认文本。

### 示例

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
