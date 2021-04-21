---
description: 要通过非由Livefyre应用程序触发的流向Livefyre验证用户身份，Livefyre建议您在AuthDelegate对象上实现forEachAuthentication方法。
title: 实施SSO
exl-id: 9af75b8a-9d2a-446e-8cce-2de8645038f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# 实施SSO{#implementing-sso}

要通过非由Livefyre应用程序触发的流向Livefyre验证用户身份，Livefyre建议您在AuthDelegate对象上实现forEachAuthentication方法。

将在将`authDelegate`传递到`auth.delegate`时调用此值，并将传递可多次传递的验证函数。 此方法提供对身份验证事件的控制反转，以便您的`AuthDelegateobject`可以自包含，而不需要对身份验证的全局引用。

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre依靠用户令牌来协调身份验证。 因此，您的身份服务必须返回此令牌才能使用Livefyre验证用户身份。 要了解如何创建Livefyre用户令牌，请参阅构建用户身份验证令牌。

>[!NOTE]
>
>成功登录后，auth将为用户创建会话，并将尝试在页面刷新和重新加载时加载用户的会话。 `auth.logout()` 将清除此会议。这意味着不必独立于授权管理用户的会话。
