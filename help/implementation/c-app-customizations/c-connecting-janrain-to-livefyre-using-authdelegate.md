---
description: Livefyre. needs提供一个插件，可让用户收听Janrain Backflane总线。
seo-description: Livefyre. needs提供一个插件，可让用户收听Janrain Backflane总线。
seo-title: 使用Authegate将Janrain连接到Livefyre
title: 使用Authegate将Janrain连接到Livefyre
uuid: 9d56e3f4-960a-4108-aab5-2795b0 e71 c88
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 使用Authegate将Janrain连接到Livefyre{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre. needs提供一个插件，可让用户收听Janrain Backflane总线。

当标识/登录消息在Backflight渠道中广播时，将为您使用用户的Livefyre身份验证令牌调用auth. authenticate()。您必须仍然执行一个authDelegate。

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>必须在页面上定义. Backflight对象，然后才能调用带有Livefyre Backflight插件的auth. plugin。要确保Backflight对象可用，请从onReady回调调用Livefyre实例化代码。请咨询您的Janrain联系人以确定其他应用程序何时使用Backflight对象。

以下示例列举了一个身份验证委托如何查找Janrain Capture集成。

>[!NOTE]
>
>根据您的Janrain实例，您的身份委托将有所不同。

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* 传递给您的身份验证委托的登录方法的回调
* 对您的Janrain捕捉变量的引用。
* ：对您的Backflight对象的引用。

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

注销

* **finishlogout：** 传递给您的身份验证委托的登录方法的回调。

* **window. Backflight：** 对您的Backflight对象的引用。

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

编辑配置文件

此链接可链接到您希望用户访问其个人资料页面的任何站点部分。此示例仅打印传入的作者对象。

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

查看配置文件

与编辑配置文件一样，这应该链接到用户的页面，该页面与当前登录用户的页面不同。但是，您可以根据需要实现此操作。此示例只将author参数记录到控制台。

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

