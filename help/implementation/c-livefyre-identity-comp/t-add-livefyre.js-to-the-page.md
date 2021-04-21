---
description: Livefyre.js是一个小型基库，可为您网站上的应用程序提供身份验证。
title: 将Livefyre.js添加到页面
exl-id: 4c5dfb31-b7e5-48f7-826c-cddbee06d876
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---

# 将Livefyre.js添加到页面{#add-livefyre-js-to-the-page}

Livefyre.js是一个小型基库，可为您网站上的应用程序提供身份验证。

要启用身份验证，请执行以下操作：

1. 将Livefyre.js添加到网页或网站模板的`<head>`元素。
1. 将以下任一内容添加到您的页面：

   * `globalwindow.Livefyre` 变量
   * `Livefyre.require` 以按需加载其他Livefyre包

      ```
      <script src="//cdn.livefyre.com/Livefyre.js"></script>
      ```
