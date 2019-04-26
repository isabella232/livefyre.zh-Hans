---
description: 安装身份验证包以启用用户身份验证，以便用户能够与您的应用程序交互。
seo-description: 安装身份验证包以启用用户身份验证，以便用户能够与您的应用程序交互。
seo-title: 身份验证包
solution: Experience Manager
title: 身份验证包
uuid: 4eec30cf-66d6-408d-985d-3e23b8b70d01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 身份验证包{#authentication-package}

安装身份验证包以启用用户身份验证，以便用户能够与您的应用程序交互。

Livefyre Apps使用全球身份验证包将用户与App操作关联。可通过身份验证包获取身份验证包 `Livefyre.require`。

要在页面上启用身份验证，请先添加 `Livefyre.js` 到网页或网站模板的 `<head>` 元素。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

使用Livefyre.要求启用身份验证类似于调用其他包。需要的集成代码如下所示：

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## 方法 {#section_ojx_1lz_fz}

在使用 `Livefyre.require`上述方法后，Auth模块会显示下列方法，您可以调用这些方法在页面上通知其他应用程序以与身份验证相关的事件。

| 方法 | 描述 |
|--- |--- |
| `.login(callback)` | 触发由已注册的authDelegate实现的登录流程。通常只有支持身份验证的应用程序才会调用此功能，而不是主机页面本身。 |
| `.logout(callback)` | 通知指出最终用户已通过某些外部方式注销，并且所有依赖应用程序都应清除其身份验证状态，直到下一次登录为止。这将清除由Auth维护的内部会话。 |
| `.authenticate(credentials)` | 通知Ath，用户已通过某些外部方式进行身份验证，并且已为最终用户购买Livefyre身份验证令牌。如果您使用Livefyre令牌设置cookie，或有用户的令牌并希望显式记录用户，请使用此方法。例如： <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | 将身份验证的实施细节(例如，您的自定义身份验证流)委派给您定义的对象。主机页面必须调用此设置才能启用Livefyre应用程序的交互功能。 |

