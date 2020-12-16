---
description: 使用Janrain Capture和底板的客户可能使用Livefyre Auth for Single Sign On(SSO)，使用户在登录您的站点时能够立即与您的Livefyre应用程序互动。
seo-description: 使用Janrain Capture和底板的客户可能使用Livefyre Auth for Single Sign On(SSO)，使用户在登录您的站点时能够立即与您的Livefyre应用程序互动。
seo-title: Janrain捕获／底板
solution: Experience Manager
title: Janrain捕获／底板
uuid: 776e9626-db04-4c34-adfe-681a71b552c5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 1%

---


# Janrain Capture/Backplane{#janrain-capture-backplane}

使用Janrain Capture和底板的客户可能使用Livefyre Auth for Single Sign On(SSO)，使用户在登录您的站点时能够立即与您的Livefyre应用程序互动。

要从此内置的Capture/Backplane集成受益，您必须对Capture应用程序和Livefyre.js集成进行配置更改。

>[!NOTE]
>
>如果您不使用Janrain Capture，请跳过此部分。

有关详细信息，请参阅[Janrain的底板文档](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/)。

1. [设置捕捉。](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. （可选）[将Livefyre默认值添加到Capture App](#c_janrain_capture_backplane/section_z2s_txt_bbb)。
1. [构建AuthDelegate对象。](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [使用Ping for Pull同步到Livefyre。](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## 第1步：设置捕获{#section_r2f_kxt_bbb}

Livefyre需要Janrain Capture应用程序中的特定凭据。

1. 设置Janrain Capture应用程序。
1. 收集Livefyre的以下信息：

   * 访问您的Janrain Capture实例。
   * 与Janrain互动仪表板。
   * 您的捕获设置和凭据。
   * 您的参与凭据。
   * 您的身份URL。

>[!NOTE]
>
>Livefyre直接从CNAME接收数据；因此，此标识URL不能是解析为Janrain Capture的实际CNAME的CNAMEd记录（虚URL CNAME）。

## 第2步：（可选）将Livefyre默认值添加到您的Capture App {#section_z2s_txt_bbb}

将Livefyre默认值添加到存储在Capture应用程序中的用户，以使您能够向用户发送电子邮件通知或允许用户自动关注用户评论的对话。

1. 完成[步骤1:设置捕获](#c_janrain_capture_backplane/section_r2f_kxt_bbb)。
1. 添加以下Livefyre默认字段。 所有字段都是可选字段。

| 参数 | 类型 | 描述 |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | 字符串 | 当有人评论文章时通知用户他们正在关注。 可以立即、经常或从不。 |
| **[!UICONTROL livefyre_likes]** | 字符串 | 当某人喜欢其某个帖子时通知用户。 可以立即、经常或从不。 |
| **[!UICONTROL livefyre_replies]** | 字符串 | 当某人回复其某个帖子时通知用户。可以立即、经常或从不。 |
| **[!UICONTROL livefyre_moderator_comments]** | 字符串 | 当某人对对话进行评论时通知主持人他们正在协调。可以立即、经常，也可以从不。 |
| **[!UICONTROL livefyre_moderator_flags]** | 字符串 | 当某人标记对话中的帖子时通知主持人他们正在协调。可以立即、经常或从不。 |
| **[!UICONTROL livefyre_autofollow_conversations]** | 布尔值 | 让用户在离开帖子时自动关注对话。 可以是true或false。 |

## 第3步：为Janrain集成构建AuthDelegate对象{#section_asv_vyt_bbb}

Livefyre.require提供一个插件，允许身份验证监听Janrain底板总线。

### 登录 {#login}

当在底板渠道广播身份／登录消息时，将使用用户的Livefyre身份验证令牌为您调用auth.authenticate()。 您仍必须实施AuthDelegate。

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
>在使用Livefyre底板插件调用auth.plugin之前，必须在页面上定义window.Backplane对象。 要确保底板对象可用，请从onReady回调中调用Livefyre实例化代码。 请咨询Janrain联系人，确定其他应用程序何时可以使用底板对象。



>[!NOTE]
>
>您的身份验证委托将因您的Janrain实例而异。

以下是身份验证委托如何查找Janrain Capture集成的一些示例。

* `errback`:传递给身份验证委托的登录方法的回调
* `janrain`:对Janrain捕获变量的引用。
* `window.Backplane`:对底板对象的引用。

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

* `finishLogout`:传递给身份验证委托的登录方法的回调。

* `window.Backplane`:对底板对象的引用。

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

### 编辑个人资料 {#editprofile}

这可以链接到您希望用户访问网站的任何部分，以视图其自己的用户档案页面。 此示例仅打印传入的作者对象。

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

### 视图用户档案{#viewprofile}

与“编辑”用户档案类似，该链接应链接到与当前登录用户不同的用户页面。 无论您认为如何适合，都可以实现此功能。 此示例只将作者参数记录到控制台。

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## 第4步：通过Ping for Pull for Janrain Integration {#section_ilv_bzt_bbb}同步到Livefyre

使Livefyre远程用户档案与Capture用户管理系统保持同步需要执行一系列步骤，称为Ping for Pull。 此过程要求您从Janrain获得有效访问令牌，然后将该令牌传递给下面步骤3中指定的端点。

1. 从Janrain获取访问代码。

   要获取访问代码，请提供必要的凭据，将user_type指定为“user”，将uuid指定为当前用户的uuid进行更新。 有关详细信息，请参阅[https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/)。

1. 为访问令牌交换访问代码。 提供必需的凭据、从步骤1接收的访问代码，并将grant_type指定为“authorization_code”。

   有关详细信息，请参阅[https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/)。

1. 点击Livefyre“Ping to Pull Capture”端点。

   端点URL:[!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}]其中&#x200B;***{networkName}***&#x200B;是Livefyre提供给您的网络名称，而jrtoken是步骤2中从Janrain接收的令牌。

   点击此端点后，您会收到202响应，Livefyre将开始异步过程。

## 全部工作方式{#concept_mty_f31_2cb}

要从此内置的Capture/Backplane集成受益，您必须对Capture应用程序和Livefyre.js集成进行一些配置更改。

Janrain通过底板总线发送成功的登录／注销消息，Livefyre应用程序在其上正确配置后会监听该总线。 这些消息包含显示应用程序用户已登录或已注销所需的所有信息。 开发人员可以通过检查浏览器的开发人员控制台中的“网络”选项卡来视图底板总线消息。

## 登录代码示例{#section_ftt_tvp_mz}

请求:

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

响应:

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

## 注销代码示例{#section_t52_svp_mz}

请求:

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

响应:

```
Backplane.finishInit("{CHANNEL}");
```

如果这些消息未出现在您的网络请求中，Livefyre将不会收到登录／注销尝试，因此，Livefyre将无法将用户集成到应用程序中。
