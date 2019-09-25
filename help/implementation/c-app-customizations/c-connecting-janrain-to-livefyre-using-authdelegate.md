---
description: Livefyre.require提供了一个插件，它使身份验证能够监听Janrain底板总线。
seo-description: Livefyre.require提供了一个插件，它使身份验证能够监听Janrain底板总线。
seo-title: 使用AuthDelegate将Janrain连接到Livefyre
title: 使用AuthDelegate将Janrain连接到Livefyre
uuid: 9d56e3f4-960a-4108-aab5-2795b0e71c88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 使用AuthDelegate将Janrain连接到Livefyre{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre.require提供了一个插件，它使身份验证能够监听Janrain底板总线。

当在底板通道上广播标识／登录消息时，将使用用户的Livefyre身份验证令牌为您调用auth.authenticate()。 您仍必须实施AuthDelegate。

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
>在使用Livefyre Backplane插件调用auth.plugin之前，必须在页面上定义window.Backplane对象。 要确保Backplane对象可用，请从onReady回调中调用Livefyre实例化代码。 请咨询Janrain联系人，以确定其他应用程序何时可以使用底板对象。

以下是身份验证委托如何查找Janrain Capture集成的一些示例。

>[!NOTE]
>
>您的身份验证委托因您的Janrain实例而异。

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* 传递给身份验证委托的登录方法的回调
* 对Janrain捕获变量的引用。
* :对底板对象的引用。

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

* **** finishLogout:传递给身份验证委托的登录方法的回调。

* **** window.底板：对底板对象的引用。

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

编辑个人资料

这可以链接到您希望用户访问站点的任何部分，以查看其自己的配置文件页面。 此示例仅打印传入的作者对象。

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

与“编辑配置文件”一样，该配置文件应链接到与当前登录用户不同的用户页面。 无论您认为如何，都可以实现此功能。 此示例只将作者参数记录到控制台。

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

