---
description: 将自定义操作添加到Livefyre应用程序。
seo-description: 将自定义操作添加到Livefyre应用程序。
seo-title: 添加自定义按钮
solution: Experience Manager
title: 添加自定义按钮
uuid: 27d24c21-d83f-49df-9b3f-15d7abbd2bd7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# 添加自定义按钮{#add-custom-buttons}

将自定义操作添加到Livefyre应用程序。

Livefyre允许您在某条内容的现有操作按钮（如&#x200B;**[!UICONTROL Share]**&#x200B;和&#x200B;**[!UICONTROL Flag]**）旁添加自定义按钮。

使用mobile参数定义按钮是否将显示在移动设备上。

例如，要为移动设备界面添加自定义操作按钮：

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

1. 在名为actionButtons的ConvConfig对象中传递一个附加参数，其中包含一组对象，用于描述要添加的每个按钮。
1. 定义要为每个按钮显示的文本的键。
1. 添加一个回调，该回调将在每个按钮的单击事件中调用。

使用具有两个键的对象调用回调：`authorId`和`contentId`。
