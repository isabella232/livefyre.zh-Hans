---
description: 使用Livefyre.js为Livefyre应用程序添加页面范围身份验证。
title: 使用Livefyre.js将身份验证添加到应用程序
exl-id: 6246a2bc-e7ff-4f86-a63a-36261c71d460
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 使用Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}将身份验证添加到应用程序

使用Livefyre.js为Livefyre应用程序添加页面范围身份验证。

`Livefyre.js Aut`h是由Livefyre开发的JavaScript包，它使您网站上的所有应用程序共享单个身份验证集成。Auth允许您通过将这些流委派到您定义的AuthDelegate对象来定义用户应如何注册、登录和注销。

## 第1步：为页面{#section_pgp_jtt_bbb}启用身份验证

使用`Livefyre.js`为页面启用身份验证，以便允许用户使用您现有的身份验证系统登录并与应用程序交互。

1. 要在页面上启用身份验证，请将`Livefyre.js`添加到网页或网站模板的&#x200B;*&lt;head>*&#x200B;元素。

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. 使用`Livefyre.require`启用身份验证。 使用`Livefyre.require`与使用要求调用其他包类似。 需要身份验证的集成代码如下所示：

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## 第2步：注册AuthDelegate {#section_oqm_15t_bbb}

要启用身份验证，请创建`AuthDelegate`并将其传递给`Livefyre.js`身份验证。

`AuthDelegate`是您定义的一个对象，它确定用户将如何登录、注销和视图用户档案。

1. 创建 `AuthDelegate`. 构建`AuthDelegate`的方式取决于您的标识提供者。 有关更多详细说明，请参阅身份集成。

1. 将`AuthDelegate`传递到`Livefyre.js`身份验证。 只要用户从App触发委托登录方法，最简单的`AuthDelegate`将同一用户登录：

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## 第3步：同步用户数据{#section_u4m_j5t_bbb}

在Livefyre和您的标识提供者之间同步用户用户档案信息。

您必须在Livefyre和您的标识提供者之间同步您的用户用户档案信息。 有关详细信息，请参阅[Janrain Capture Integration](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)。
