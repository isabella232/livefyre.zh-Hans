---
description: Livefyre.js身份验证包可确保页面上的所有社交组件都能够发现单个身份验证集成。
seo-description: Livefyre.js身份验证包可确保页面上的所有社交组件都能够发现单个身份验证集成。
seo-title: 初始化Livefyre标识
title: 初始化Livefyre标识
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# 初始化Livefyre Identity{#initialize-livefyre-identity}

Livefyre.js身份验证包可确保页面上的所有社交组件都能够发现单个身份验证集成。

Livefyre提供一个`lfep-auth-delegate`包，它将为您提供一个适当的身份验证委托。 必须为AuthDelegate对象提供身份验证，该对象知道如何执行身份验证操作，如登录和注销。

1. 将Livefyre.js添加到您的网页。
1. 要告知Auth将这些操作委派到Livefyre Identity，请添加以下内容：

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
