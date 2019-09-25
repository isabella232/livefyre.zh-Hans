---
description: 使用Livefyre.js为Livefyre应用程序添加页面范围身份验证。
seo-description: 使用Livefyre.js为Livefyre应用程序添加页面范围身份验证。
seo-title: 使用Livefyre.js将身份验证添加到应用程序
solution: Experience Manager
title: 使用Livefyre.js将身份验证添加到应用程序
uuid: b7c61e07-e341-45d7-9112-c50155e38f1d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc

---


# 使用Livefyre.js将身份验证添加到应用程序{#add-authetication-to-an-app-using-livefyre-js}

使用Livefyre.js为Livefyre应用程序添加页面范围身份验证。

`Livefyre.js Aut`h是由Livefyre开发的JavaScript包，它使您网站上的所有应用程序能够共享单个身份验证集成。 Auth允许您通过将这些流委派到您定义的AuthDelegate对象来定义用户应如何注册、登录和注销。

## 第1步：启用页面身份验证 {#section_pgp_jtt_bbb}

使用 `Livefyre.js` 为页面启用身份验证，以便允许用户使用现有的身份验证系统登录并与应用程序交互。

1. 要在页面上启用身份验证， `Livefyre.js` 请添加 *到网页或网站模板的* &lt;head&gt;元素。

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. 使用 `Livefyre.require` 启用身份验证。 使用 `Livefyre.require` 与使用要求调用其他包类似。 需要身份验证的集成代码如下所示：

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## 第2步：注册AuthDelegate {#section_oqm_15t_bbb}

要启用身份验证，请创 `AuthDelegate` 建并将其传递给 `Livefyre.js` 身份验证。

您定 `AuthDelegate` 义的对象用于确定用户如何登录、注销和查看配置文件。

1. 创建 `AuthDelegate`. 您构建方式取决 `AuthDelegate` 于您的标识提供者。 有关更详细的说明，请参阅身份集成。

1. 将此信息传 `AuthDelegate` 递到 `Livefyre.js` 身份验证。 每当用 `AuthDelegate` 户从应用程序触发委托登录方法时，最简单的登录方式是：

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## 第3步：同步用户数据 {#section_u4m_j5t_bbb}

在Livefyre和您的标识提供者之间同步用户配置文件信息。

您必须在Livefyre和您的标识提供者之间同步用户配置文件信息。 有关详细信息，请参 [阅Janrain Capture集成](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)。
