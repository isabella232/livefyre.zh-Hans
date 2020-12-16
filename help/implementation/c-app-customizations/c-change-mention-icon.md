---
description: 更改 @mention 下拉菜单中为 Livefyre 用户显示的图标。
seo-description: 更改 @提及下拉菜单中为 Livefyre 用户显示的图标。
seo-title: 更改 @提及图标
solution: Experience Manager
title: 更改 @mention 图标
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 31%

---


# 更改`@mention`图标{#change-mention-icon}

在`@mention`下拉菜单中更改为Livefyre用户显示的图标。

将`@mention`下拉菜单中使用的Livefyre图标更改为您选择的图标，这样您便可以使用自己的图标指示社区成员。

## 示例

要更改此图标，请向样式表添加以下CSS。 将资源&#x200B;*url替换为选定用于替换默认Livefyre徽章的图像URL。*

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
