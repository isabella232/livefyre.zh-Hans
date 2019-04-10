---
description: 使用Livefyre. js为Livefyre应用程序添加页面范围的身份验证。
seo-description: 使用Livefyre. js为Livefyre应用程序添加页面范围的身份验证。
seo-title: 使用Livefyre. js向应用程序添加自动连接
solution: Experience Manager
title: 使用Livefyre. js向应用程序添加自动连接
uuid: b7c61e07-e341-45d7-9112-c50155 e38 f1 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 使用Livefyre. js为应用程序添加身份验证{#add-authetication-to-an-app-using-livefyre-js}

使用Livefyre. js为Livefyre应用程序添加页面范围的身份验证。

`Livefyre.js Aut`h是Livefyre开发的一个JavaScript包，它允许您网站上的所有应用程序共享单一身份验证集成。Auth允许您定义用户如何注册、登录和注销，方法是将这些流委派给您定义的AuthDelate对象。

## 步骤1：为页面启用身份验证 {#section_pgp_jtt_bbb}

用于 `Livefyre.js` 启用页面身份验证，以便允许用户使用现有身份验证系统登录并与应用程序交互。

1. 要在页面上启用身份验证，请添加 `Livefyre.js` 到网页或网站模板的 *< head>* 元素。

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. 用于 `Livefyre.require` 启用身份验证。使用 `Livefyre.require` 类似于使用需要调用其他包。需要的集成代码如下所示：

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## 步骤2：注册一个authDelegate {#section_oqm_15t_bbb}

要启用身份验证，请创建一个身份 `AuthDelegate` 验证并将其传递 `Livefyre.js` 给身份验证。

是 `AuthDelegate` 您定义的一个对象，用于确定用户如何登录、注销和查看配置文件。

1. 创建 `AuthDelegate`一个。您构建的 `AuthDelegate` 方式取决于标识提供者。有关更多详细说明，请参阅标识集成。

1. 传递 `AuthDelegate``Livefyre.js` 到身份验证。当用户从应用程序触发委托登录方法时，最简单 `AuthDelegate` 的方法是将同一用户登录到该应用程序：

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## 步骤3：同步用户数据 {#section_u4m_j5t_bbb}

同步Livefyre与您的标识提供者之间的用户配置文件信息。

您必须在Livefyre和您的标识提供者之间同步用户配置文件信息。有关更多信息，请参阅 [Janrain Capture集成](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)。
