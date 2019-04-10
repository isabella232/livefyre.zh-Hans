---
description: 将自定义操作添加到Livefyre应用程序。
seo-description: 将自定义操作添加到Livefyre应用程序。
seo-title: 添加自定义按钮
solution: Experience Manager
title: 添加自定义按钮
uuid: 27d24c21-d83 f-49df-9b3 f-15d7 abbd2 bd7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 添加自定义按钮{#add-custom-buttons}

将自定义操作添加到Livefyre应用程序。

Livefyre允许您在内容的现有操作按钮(如 **[!UICONTROL Share]**和 **[!UICONTROL Flag]**)上添加自定义按钮。

使用移动参数定义按钮是否将显示在移动设备上。

例如，为移动设备界面添加自定义操作按钮：

```
var convConfig = {...}; // Should have siteId, articleId, etc. 
convConfig.actionButtons = [ 
   { 
      mobile: true,  
      // (optional) sets whether the button will appear on mobile devices 
      key: 'Do Something', 
      callback: function(contentInfo) { 
         console.log('Author of content is ' + contentInfo.authorId); 
         console.log('id of content is ' + contentInfo.contentId); 
      } 
   }, 
    ... 
]; 
  
fyre.conv.load(networkConfig, [convConfig]);
```

1. 在名为actionButtons的OverConfig对象中传递另一个参数，其中包含一组对象，这些对象描述要添加的每个按钮。
1. 为每个按钮显示要显示的文本。
1. 添加一个回调，该回调将在每个按钮的单击事件上调用。

将使用具有两个键的对象调用回调： `authorId``contentId`和.
