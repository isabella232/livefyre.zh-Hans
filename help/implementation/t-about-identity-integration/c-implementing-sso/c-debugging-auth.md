---
description: 在集成和测试过程中，可以通过控制台登录用户以调试授权。
seo-description: 在集成和测试过程中，可以通过控制台登录用户以调试授权。
seo-title: 调试身份验证委托
solution: Experience Manager
title: 调试身份验证委托
uuid: fb0c7396-190e-4dc9-bf26-23dde9efd45d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 调试身份验证委托{#debugging-auth-delegate}

在集成和测试过程中，可以通过控制台登录用户以调试授权。

使用以下（令牌）将用户通过控制台登 `auth.authenticate` 录，并传递Livefyre用户令牌以验证页面上的用户身份。

您还可以修改上面显示的示例，并在JavaScript中内嵌以下代码片断，以快速将用户登录Livefyre（需要引用auth）。

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

