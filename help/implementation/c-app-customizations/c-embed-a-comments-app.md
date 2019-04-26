---
description: 嵌入评论应用程序会遵循嵌入核心应用程序的过程。
seo-description: 嵌入评论应用程序会遵循嵌入核心应用程序的过程。
seo-title: 嵌入评论应用程序
solution: Experience Manager
title: 嵌入评论应用程序
uuid: e4982ad3-cab1-4805-a55 c-594ca3 b7203
translation-type: tm+mt
source-git-commit: 268dc91369d346a254b7120706264eb91da8257e

---


# 嵌入评论应用程序{#embed-a-comments-app}

嵌入评论应用程序会遵循嵌入核心应用程序的过程。

嵌入评论应用程序遵循嵌入应用程序中描述的核心应用程序 [的过程。](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)

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

如Building CollectionMeta部分中所述，CollectionMeta是一个编码的JSON对象。在以上示例中，JSON对象在JWT编码之前采用以下格式：

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

