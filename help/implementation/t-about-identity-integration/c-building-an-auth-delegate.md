---
description: AuthDelegate对象为如何执行身份验证操作和事件实现您所需的行为，以便自定义与站点现有身份验证系统的集成。
seo-description: AuthDelegate对象为如何执行身份验证操作和事件实现您所需的行为，以便自定义与站点现有身份验证系统的集成。
seo-title: AuthDelegate Object
solution: Experience Manager
title: AuthDelegate Object
uuid: a6acc4ef-d442-4782-9bfa-bbe494547 c2 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# AuthDelegate Object{#authdelegate-object}

AuthDelegate对象为如何执行身份验证操作和事件实现您所需的行为，以便自定义与站点现有身份验证系统的集成。

## 构建Auth Delegate {#section_wmn_tv2_gz}

必须先向身份验证包提供身份验证包，然后才能执行操作。身份委托是任何实现本主题中的某个方法的JavaScript对象。

## . login(Finishlogin) {#section_mpk_lv2_gz}

如果存在错误，或用户的Livefyre凭据，则登录有效用户并调用带有Error对象的FinishLogin函数。此方法的常见实现将用户重定向到登录页面或打开新窗口或模态。

此示例使用身份验证令牌和令牌自动通知Livefyre用户身份：

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

## . logout(finishlogout) {#section_uqz_2v2_gz}

注销用户，并在出现错误时调用finishLogout函数，或null以通知指出注销成功。

例如：

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## . ViewProfile(用户) {#section_kkv_dv2_gz}

采取措施查看用户的个人资料。

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## . EditProfile(用户) {#section_bkx_pq2_gz}

采取措施编辑用户的个人资料。

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

通过实施以上列出的所有方法，可以使用自定义身份委派配置身份验证。构造委托后，可以使用委托方法将其提供给身份验证。

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

