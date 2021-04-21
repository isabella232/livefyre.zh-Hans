---
description: Livefyre.js身份验证包可确保页面上的所有社交组件都能够发现单个身份验证集成。
title: 初始化Livefyre标识
exl-id: 9990d284-a21e-49fb-932c-62906b41484a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# 初始化Livefyre Identity{#initialize-livefyre-identity}

Livefyre.js身份验证包可确保页面上的所有社交组件都能够发现单个身份验证集成。

Livefyre提供了一个`lfep-auth-delegate`包，它将为您提供一个适当的身份验证委托。 必须为AuthDelegate对象提供AuthDelegate对象，该对象知道如何执行身份验证操作，如登录和注销。

1. 将Livefyre.js添加到您的网页。
1. 要告诉Auth将这些操作委派给Livefyre Identity，请添加以下内容：

   ```
   Livefyre.require([ 
     'livefyre-auth', 
     'identity' 
     ], function (auth, Identity) { 
       var identity = new Identity({ 
         app: "https://identity.livefyre.com/{networkName}.fyre.co" 
       }); 
    auth.delegate( identity ); 
    });
   ```
