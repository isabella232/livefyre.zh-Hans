---
description: 嵌入注释应用程序遵循嵌入核心应用程序的过程。
seo-description: 嵌入注释应用程序遵循嵌入核心应用程序的过程。
seo-title: 嵌入注释应用程序
solution: Experience Manager
title: 嵌入注释应用程序
uuid: e4982ad3-cab1-4805-a55c-594cca3b7203
translation-type: tm+mt
source-git-commit: 268dc91369d346a254b7120706264eb91da8257e
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 1%

---


# 嵌入注释应用程序{#embed-a-comments-app}

嵌入注释应用程序遵循嵌入核心应用程序的过程。

嵌入注释应用程序遵循嵌入核心应用程序（如[嵌入应用程序](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)所述）的过程

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

如构建集合元部分中所述，集合元是编码的JSON对象。 在上例中，JSON对象在进行JWT编码前采用以下格式：

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

