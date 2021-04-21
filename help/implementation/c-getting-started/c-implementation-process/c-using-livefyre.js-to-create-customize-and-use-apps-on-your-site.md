---
title: 嵌入应用程序
description: 嵌入应用程序
exl-id: 12f75093-1b4d-4cf1-8593-dbd17ff33872
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# 嵌入应用程序{#embed-an-app}

使用Livefyre.js嵌入代码结构将Livefyre应用程序添加到您的网页。

本文档旨在提供技术受众。 有关[有关应用程序的非技术信息](/help/using/c-about-apps/c-about-apps.md)。

本节介绍在您的网站上嵌入Livefyre应用程序时需要包含的代码结构。

1. 使用Livefyre占位符创建.html文件。

   在您选择的文本编辑器中新建一个.html文件。 创建一个占位符Livefyre `<div>`元素，将在其中嵌入应用程序。

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. 包括Livefyre.js库。

   然后，加入Livefyre JS库。 在`<head>`元素的`<script>`元素中放置以下引用。 然后，在浏览器中打开您的页面，并使用浏览器的Web检查器确认已加载Livefyre。

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. 构建Livefyre应用程序。

   使用`Livefyre.require`通过传入您计划使用的Livefyre包，构建核心和SDK应用程序。

   1. 构建核心应用程序。

      要构建核心应用程序（注释、实时博客或聊天），请使用以下结构：

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. 构建SDK应用程序。

      要构建SDK应用程序（如Media Wall或Feed），请使用以下结构：

      ```
             Livefyre.require(['app#{version_number}'], 
         function (App, SDK) { 
            var app = new App({ 
            el: document.getElementById('app'), 
         }); 
         var collection = new SDK.Collection({ 
            network: "`labs.fyre.co`", 
            environment: "livefyre.com", 
            siteId: "315833", 
            articleId: 'livefyre-tweets' 
         }); 
         collection.pipe(feed); 
      }); 
      ```

      有关特定Apps的详细信息，请参阅[](/help/using/c-about-apps/c-about-apps.md)。 建议您固定到该包的最新主要版本（可通过[Livefyre.require](https://cdn.livefyre.com/packages.html)找到），以避免意外中断的集成。

下一步：向您的站点添加身份验证，以使您的用户能够发布评论。
