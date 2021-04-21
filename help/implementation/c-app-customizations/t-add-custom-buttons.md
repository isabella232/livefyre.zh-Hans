---
description: 将自定义操作添加到您的Livefyre应用程序。
title: 添加自定义按钮
exl-id: a62d8605-59c2-4214-af26-805c1989aca1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# 添加自定义按钮{#add-custom-buttons}

将自定义操作添加到您的Livefyre应用程序。

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

1. 在名为actionButtons的ConvConfig对象中传递一个附加参数，其中包含一组描述要添加的每个按钮的对象。
1. 定义要为每个按钮显示的文本的键。
1. 添加一个回调，该回调将在每个按钮的单击事件中被调用。

使用具有两个键的对象调用回调：`authorId`和`contentId`。
