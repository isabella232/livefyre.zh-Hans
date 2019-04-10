---
description: 您可以在集成和测试过程中通过控制台记录用户以调试授权。
seo-description: 您可以在集成和测试过程中通过控制台记录用户以调试授权。
seo-title: 调试Auth Delegate
solution: Experience Manager
title: 调试Auth Delegate
uuid: fb0c7396-190e-4dc9-bf26-23dde9 efd45 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 调试Auth Delegate{#debugging-auth-delegate}

您可以在集成和测试过程中通过控制台记录用户以调试授权。

使用以下(令牌)通过控制台登录用户 `auth.authenticate` ，并传递Livefyre用户令牌以验证页面上的用户。

您还可以修改上面显示的示例，并在JavaScript中将下面的代码片断添加到JavaScript中，以便将用户快速记录到Livefyre(需要引用Auth)。

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

