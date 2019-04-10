---
seo-title: 嵌入应用程序
solution: Experience Manager
title: 嵌入应用程序
uuid: e75caf0e-04ea-4b04-89ed-fea1183 ef63
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 嵌入应用程序{#embed-an-app}

使用Livefyre. js嵌入代码结构将Livefyre应用程序添加到网页。

此文档适用于技术受众。有关 [应用程序](/help/using/c-about-apps/c-about-apps.md)的非技术信息。

本节介绍将需要包含在页面模板中的代码结构，以嵌入站点上的Livefyre应用程序。

1. 使用Livefyre占位符创建.html文件。

   在您选择的文本编辑器中创建一个新的.html文件。创建将嵌入应用程序的占位符Livefyre `<div>` 元素。

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. 包括Livefyre. js库。

   然后，包括Livefyre JS库。将以下引用放入元素 `<script>` 元素 `<head>` 中。然后，在浏览器中打开页面，并使用浏览器的Web检查器确认Livefyre已加载。

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. 构建Livefyre应用程序。

   使用 `Livefyre.require` 您计划使用的Livefyre包来构建核心和SDK应用程序。

   1. 构建核心应用程序。

      要构建核心应用程序(评论、Live Blog或聊天)，请使用以下结构：

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. 构建SDK应用程序。

      要构建SDK应用程序(如“媒体墙”或“源”)，请使用以下结构：

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

      查看 [有关特定应用程序](/help/using/c-about-apps/c-about-apps.md)的更多信息。建议您固定到包的最新主要版本(可通过 [Livefyre. needs](https://cdn.livefyre.com/packages.html)找到)，以避免意外损坏的集成。

下一步：向您的站点添加身份验证以使用户能够发布评论。
