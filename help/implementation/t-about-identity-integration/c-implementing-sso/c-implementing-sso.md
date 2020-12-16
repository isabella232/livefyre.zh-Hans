---
description: 要通过Livefyre应用程序未触发的流向Livefyre验证用户身份，Livefyre建议您在AuthDelegate对象上实施forEachAuthentication方法。
seo-description: 要通过Livefyre应用程序未触发的流向Livefyre验证用户身份，Livefyre建议您在AuthDelegate对象上实施forEachAuthentication方法。
seo-title: 实施SSO
solution: Experience Manager
title: 实施SSO
uuid: c96d456c-b1ac-40e0-8d18-224652b9697f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# 实施SSO{#implementing-sso}

要通过Livefyre应用程序未触发的流向Livefyre验证用户身份，Livefyre建议您在AuthDelegate对象上实施forEachAuthentication方法。

将在将`authDelegate`传递到`auth.delegate`时调用此值，并将传递一个可多次传递的身份验证函数。 此方法提供对身份验证事件的控制反转，使您的`AuthDelegateobject`可以自包含，而不需要对身份验证的全局引用。

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre依靠用户令牌来协调身份验证。 因此，您的标识服务必须返回此令牌才能使用Livefyre验证用户身份。 要了解如何创建Livefyre用户令牌，请参阅构建用户身份验证令牌。

>[!NOTE]
>
>成功登录后，身份验证将为用户创建会话，并将尝试在页面刷新和重新加载时加载用户的会话。 `auth.logout()` 会议将结束。这意味着不必独立于授权管理用户的会话。

