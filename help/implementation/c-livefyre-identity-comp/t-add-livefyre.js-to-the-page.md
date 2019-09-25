---
description: Livefyre.js是一个小型基本库，可为站点上的应用程序提供身份验证。
seo-description: Livefyre.js是一个小型基本库，可为站点上的应用程序提供身份验证。
seo-title: 将Livefyre.js添加到页面
title: 将Livefyre.js添加到页面
uuid: fe52446e-4911-4160-a68c-7413e9bc6222
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 将Livefyre.js添加到页面{#add-livefyre-js-to-the-page}

Livefyre.js是一个小型基本库，可为站点上的应用程序提供身份验证。

要启用身份验证，请执行以下操作：

1. 将Livefyre.js添加到网 `<head>` 页或网站模板的元素中。
1. 将以下任一内容添加到您的页面：

   * `globalwindow.Livefyre` 变量
   * `Livefyre.require` 按需加载其他Livefyre包

      ```
      <script src="//cdn.livefyre.com/Livefyre.js"></script>
      ```

