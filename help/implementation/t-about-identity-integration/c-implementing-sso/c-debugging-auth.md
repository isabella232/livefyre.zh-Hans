---
description: 在进行集成和测试以调试授权时，您可以通过控制台登录用户。
title: 调试身份验证委派
exl-id: fa1c17fa-5aba-4f4c-9217-5823af30af61
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# 调试身份验证委派{#debugging-auth-delegate}

在进行集成和测试以调试授权时，您可以通过控制台登录用户。

使用以下`auth.authenticate`（令牌）通过控制台登录，并传递Livefyre用户令牌以验证页面上的用户。

您还可以修改上面显示的示例，并在JavaScript中串联添加以下代码片断，以快速将用户登录Livefyre（需要对auth的引用）。

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```
