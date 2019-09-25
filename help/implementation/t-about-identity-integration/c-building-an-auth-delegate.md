---
description: AuthDelegate对象实现了您所需的行为，用于了解如何执行身份验证操作和事件，以便您可以自定义与站点现有身份验证系统的集成。
seo-description: AuthDelegate对象实现了您所需的行为，用于了解如何执行身份验证操作和事件，以便您可以自定义与站点现有身份验证系统的集成。
seo-title: 身份验证委托对象
solution: Experience Manager
title: 身份验证委托对象
uuid: a6acc4ef-d442-4782-9bfa-bbe494547c2e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 身份验证委托对象{#authdelegate-object}

AuthDelegate对象实现了您所需的行为，用于了解如何执行身份验证操作和事件，以便您可以自定义与站点现有身份验证系统的集成。

## 构建身份验证委托 {#section_wmn_tv2_gz}

必须先向身份验证包提供身份验证委托，然后才能执行操作。 身份验证委托是实现本主题中某个方法的任何JavaScript对象。

## .login(finishLogin) {#section_mpk_lv2_gz}

登录有效用户，并在出现错误时使用Error对象调用finishLogin函数，或者调用用户的Livefyre凭据。 此方法的常见实现将用户重定向到登录页面或打开新窗口或模式。

此示例自动通知具有身份验证令牌（令牌）的Livefyre用户的身份验证：

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

最简单的登录委托可能会向最终用户询问其Livefyre身份验证令牌。

```
authDelegate.login = function contrivedLogin(finishLogin) { 
  var lfToken = prompt("Please type your Livefyre Token");  
  if (lfToken.length === 0) { 
   return finishLogin(new Error("User failed to type their lftoken")); 
  }  
 finishLogin(null, { 
   livefyre: lfToken 
 }); 
};
```

## .logout(finishLogout) {#section_uqz_2v2_gz}

注销用户，如果出现错误，则使用Error对象调用finishLogout函数；如果出错，则使用null通知auth注销成功。

例如：

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile（用户） {#section_kkv_dv2_gz}

采取操作以查看用户的配置文件。

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile（用户） {#section_bkx_pq2_gz}

采取操作以编辑用户的配置文件。

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

通过实施上述所有方法，可以使用自定义身份验证委托配置身份验证。 构建委托后，可以向它提供使用委托方法进行身份验证。

```
var authDelegate = { 
 login: function(cb) { 
  ... 
  cb(null); 
 }, 
 ... 
} 
  
auth.delegate(authDelegate);
```

