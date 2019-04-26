---
description: Livefyre. js Auth包可确保页面上的所有社交组件都能发现单一身份验证集成。
seo-description: Livefyre. js Auth包可确保页面上的所有社交组件都能发现单一身份验证集成。
seo-title: 初始化Livefyre Identity
title: 初始化Livefyre Identity
uuid: 9365d827-2734-4a84-bfe7-9be573 b2 b03 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 初始化Livefyre Identity{#initialize-livefyre-identity}

Livefyre. js Auth包可确保页面上的所有社交组件都能发现单一身份验证集成。

Livefyre提供一个 `lfep-auth-delegate` 包，它会为您制作合适的身份委托。必须提供一个AuthDelegate对象，它知道如何执行身份验证操作(如登录和注销)。

1. 将Livefyre. js添加到您的网页。
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
