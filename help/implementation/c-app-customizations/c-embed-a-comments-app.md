---
description: 嵌入注释应用程序遵循嵌入核心应用程序的过程。
title: 嵌入注释应用程序
exl-id: 5eb191f8-ee52-4a9d-9180-90457a49fd4e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# 嵌入注释应用程序{#embed-a-comments-app}

嵌入注释应用程序遵循嵌入核心应用程序的过程。

嵌入注释应用程序遵循嵌入核心应用程序（如[嵌入应用程序](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)中所述）的过程

## 示例

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
        auth.delegate({ 
            login: function (callback) { 
                callback(null,{livefyre:'<userauthtoken>'}); 
            }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

正如构建CollectionMeta部分中所述，CollectionMeta是编码的JSON对象。 在上例中，JSON对象在进行JWT编码前采用以下格式：

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```
