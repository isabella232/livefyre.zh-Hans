---
description: 更改 @提及下拉菜单中为 Livefyre 用户显示的图标。
title: 更改 @提及图标
exl-id: e078ef7f-7f16-4f5d-9152-95ae7fe7e4bd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 19%

---

# 更改`@mention`图标{#change-mention-icon}

在`@mention`下拉菜单中更改为Livefyre用户显示的图标。

将`@mention`下拉菜单中使用的Livefyre图标更改为您选择的图标，这样您就可以使用自己的图标指示社区成员。

## 示例

要更改此图标，请向样式表添加以下CSS。 将资源&#x200B;*url*&#x200B;替换为选定用于替换默认Livefyre徽章的图像URL。

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
