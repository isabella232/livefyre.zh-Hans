---
description: Livefyre建议您在authDelegate对象上实施PreAthhentication方法，以便通过Livefyre App对用户进行身份验证。
seo-description: Livefyre建议您在authDelegate对象上实施PreAthhentication方法，以便通过Livefyre App对用户进行身份验证。
seo-title: 实施SSO
solution: Experience Manager
title: 实施SSO
uuid: c96d456c-b1 ac-40e0-8d18-22652b9697 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 实施SSO{#implementing-sso}

Livefyre建议您在authDelegate对象上实施PreAthhentication方法，以便通过Livefyre App对用户进行身份验证。

将在传递给 `authDelegate``auth.delegate`该函数时调用该调用，并将传递一个可多次传递的身份验证函数。此方法为身份验证事件提供了反向控制，使您 `AuthDelegateobject` 无需全局引用即可自包含。

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre依靠用户令牌来协调身份验证。因此，您的标识服务必须返回此令牌才能使用Livefyre验证用户身份。要了解如何创建Livefyre用户令牌，请参阅构建用户身份验证令牌。

>[!NOTE]
>
>成功登录后，身份验证将为用户创建一个会话，并在页面刷新和重新加载时尝试加载用户的会话。`auth.logout()` 将清除此会话。这意味着不必对用户的会话单独进行授权管理。

