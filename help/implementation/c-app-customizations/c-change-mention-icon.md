---
description: 更改 @mention 下拉菜单中为 Livefyre 用户显示的图标。
seo-description: 更改 @提及下拉菜单中为 Livefyre 用户显示的图标。
seo-title: 更改 @提及图标
solution: Experience Manager
title: 更改 @mention 图标
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5

---


# 更改图 `@mention` 标 {#change-mention-icon}

Change the icon displayed for Livefyre users in the `@mention` pulldown menu.

将下拉菜单中使用的Livefyre图标更 `@mention` 改为您选择的图标，以便用您自己的图标指示社区成员。

## 示例

要更改此图标，请将以下CSS添加到样式表。 将&lt;您&#x200B;*的资源*&gt; url替换为所选图像的URL以替换默认的Livefyre徽章。

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
