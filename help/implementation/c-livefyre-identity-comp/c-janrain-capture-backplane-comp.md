---
description: 使用Janrain Capture和Backflight的客户可使用Livefyre Auth for Single Sign On(SSO)，以便用户在登录您的站点时立即与您的Livefyre Apps互动。
seo-description: 使用Janrain Capture和Backflight的客户可使用Livefyre Auth for Single Sign On(SSO)，以便用户在登录您的站点时立即与您的Livefyre Apps互动。
seo-title: Janrain Capture/Backflight
solution: Experience Manager
title: Janrain Capture/Backflight
uuid: 776e9626-db04-4c34-adfe-681a71 b552 c5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Janrain Capture/Backflight{#janrain-capture-backplane}

使用Janrain Capture和Backflight的客户可使用Livefyre Auth for Single Sign On(SSO)，以便用户在登录您的站点时立即与您的Livefyre Apps互动。

要从内置Capture/Back平面集成中受益，您必须对Capture应用程序和Livefyre. js集成进行配置更改。

>[!NOTE]
>
>如果您未使用Janrain Capture，请跳过此部分。

有关更多信息，请参阅 [Janrain的Backflane文档](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/)。

1. [设置Capture。](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (可选) [将Livefyre默认值添加到Capture App](#c_janrain_capture_backplane/section_z2s_txt_bbb)。
1. [构建AuthDelegate对象。](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [使用Ting for Draw同步到Livefyre。](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## 步骤1：设置Capture {#section_r2f_kxt_bbb}

Livefyre需要您的Janrain Capture应用程序提供的特定凭据。

1. 设置Janrain Capture应用程序。
1. 收集Livefyre的以下信息：

   * 访问您的Janrain Capture实例。
   * 访问您的Janrain Engage仪表板。
   * 您的捕捉设置和凭据。
   * 您的参与凭证。
   * 您的身份URL。

>[!NOTE]
>
>Livefyre直接从CNAME接收数据；因此，此标识URL不能是一个CNANED记录(一个虚URL CNAME)，它解析到Janrain Capture的实际CNAME。

## 步骤2：(可选)将Livefyre默认为Capture应用程序 {#section_z2s_txt_bbb}

向存储在Capture应用程序中的用户添加Livefyre默认值，使您能够向用户发送电子邮件通知，或允许用户自动按照用户评论的对话进行操作。

1. 完成 [步骤1：设置Capture](#c_janrain_capture_backplane/section_r2f_kxt_bbb)。
1. 添加以下Livefyre默认字段。所有字段都是可选字段。

| 参数 | Type | 描述 |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | 字符串 | 当某人对所遵循的文章进行评论时，通知用户。可以立即、经常或从不。 |
| **[!UICONTROL livefyre_likes]** | 字符串 | 当某人喜欢某个帖子时，通知用户。可以立即、经常或从不。 |
| **[!UICONTROL livefyre_replies]** | 字符串 | 当某人回复某个帖子时通知用户。可以立即、经常或从不发送通知。 |
| **[!UICONTROL livefyre_moderator_comments]** | 字符串 | 当某人对正在协调的对话做出评论时通知主持人。可以立即、经常或从不。 |
| **[!UICONTROL livefyre_moderator_flags]** | 字符串 | 当有人标记他们正在主持的对话时，通知主持人。可以立即、经常或从不。 |
| **[!UICONTROL livefyre_autofollow_conversations]** | Boolean | 用户离开帖子后自动跟随对话。可以为true或false。 |

## 步骤3：构建Authoregate Object for Janrain集成 {#section_asv_vyt_bbb}

Livefyre. needs提供一个插件，可让用户收听Janrain Backflane总线。

### 登录名 {#login}

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



>[!NOTE]
>
>根据您的Janrain实例，您的身份委托将有所不同。

以下示例列举了一个身份验证委托如何查找Janrain Capture集成。

* `errback`：传递给您的身份验证委托的登录方法的回调
* `janrain`：对您的Janrain捕捉变量的引用。
* `window.Backplane`：对您的Backflight对象的引用。

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

### 注销 {#logout}

* `finishLogout`：传递给您的身份验证委托的登录方法的回调。

* `window.Backplane`：对您的Backflight对象的引用。

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

### 编辑配置文件 {#editprofile}

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

### 查看配置文件 {#viewprofile}

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

## 第步：通过Ping for Janrain集成同步至Livefyre {#section_ilv_bzt_bbb}

将Livefyre远程配置文件与Capture用户管理系统保持同步涉及一系列称为“ping”的步骤。此过程要求您从Janrain获得有效访问令牌，然后将该令牌传递到下面步骤中指定的端点。

1. 获取来自Janrain的访问代码。

   要获取访问代码，请提供必要的凭据，将user_ type指定为“user”，并将uuid作为当前用户的uuid进行更新。有关更多信息，请参阅 [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/)。

1. 交换访问令牌的访问代码。提供必要的凭据、从步骤接收的访问代码，并将rant_ type指定为“authorization_ code”。

   有关更多信息，请参阅 [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/)。

1. 点击Livefyre“ping捕捉捕捉”端点。

   端点URL： [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] 其中 ***，{publiskName}*** 是Livefyre提供给您的网络名称，jrtoken是第步中收到的Janrain令牌。

   到达此端点后，您将收到202响应，Livefyre将开始异步进程。

## 其全部工作原理 {#concept_mty_f31_2cb}

要从内置的Capture/Back平面集成中受益，您必须对Capture应用程序和Livefyre. js集成进行一些配置更改。

Janrain通过Backflane总线发送成功的登录/注销消息，Livefyre应用程序在正确配置时，将侦听Livefyre应用程序。这些消息包含显示应用程序用户登录或注销所需的所有信息。开发人员可以通过在浏览器的开发人员控制台中检查“网络”选项卡来查看Backflight总线消息。

## 登录代码示例 {#section_ftt_tvp_mz}

请求：

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

答复：

```
Backplane.response([{ 
  "id": "2014-05-06T22:51:55.406Z-eZp1HB1F7B", 
  "channel_name": "{CHANNEL_NAME}", 
  "message": { 
    "source": "https://{CUSTOMER_DOMAIN}", 
    "type": "identity/login", 
    "sticky": true, 
    "payload": { 
      "context": "https://{CUSTOMER_DOMAIN}", 
      "identities": { 
        "startIndex": 0, 
        "itemsPerPage": 1, 
        "totalResults": 1, 
        "entry": { 
          "id": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
          "displayName": "{USER_DISPLAY_NAME}", 
          "accounts": [ 
            { 
              "username": "{USER_DISPLAY_NAME}", 
              "identityUrl": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
              "photos": [ 
                { 
                  "id": 48570146, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "other" 
                }, 
                { 
                  "id": 48570147, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "original" 
                }, 
                { 
                  "id": 48570148, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "large" 
                }, 
                { 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "avatar" 
                } 
              ] 
            }, 
            { 
              "identityUrl": "{USER_PROFILE_LINK}" 
            } 
          ] 
        } 
      } 
    } 
  } 
} 
]);
```

空响应：

```
Backplane.response([]);
```

## 注销代码示例 {#section_t52_svp_mz}

请求：

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

答复：

```
Backplane.finishInit("{CHANNEL}");
```

如果这些消息未出现在您的网络请求中，Livefyre将不会了解登录/注销尝试，因此Livefyre无法将用户集成到应用程序中。
