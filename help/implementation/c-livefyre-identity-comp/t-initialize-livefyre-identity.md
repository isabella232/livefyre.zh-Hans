---
description: Livefyre.js身份验证包可确保页面上的所有社交组件都能够发现单个身份验证集成。
seo-description: Livefyre.js身份验证包可确保页面上的所有社交组件都能够发现单个身份验证集成。
seo-title: Initialize Livefyre Identity
title: 初始化Livefyre标识
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 初始化Livefyre标识{#initialize-livefyre-identity}

Livefyre.js身份验证包可确保页面上的所有社交组件都能够发现单个身份验证集成。

Livefyre提供了一 `lfep-auth-delegate` 个包，它将为您提供一个适当的身份验证委托。 Auth must be provided an AuthDelegate object that knows how to perform authentication actions, like login and logout.

1. 将Livefyre.js添加到您的网页。
1. 要告知Auth将这些操作委派给Livefyre Identity，请添加以下内容：

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
