---
description: 在您的页面上重新定位Livefyre徽标。
seo-description: 在您的页面上重新定位Livefyre徽标。
seo-title: 移动Livefyre徽标
solution: Experience Manager
title: 移动Livefyre徽标
uuid: 807304ae-6070-4505-87db-169a925f714c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---


# 移动Livefyre徽标{#move-the-livefyre-logo}

在您的页面上重新定位Livefyre徽标。

如果您与Livefyre的协议允许，您可以将Livefyre徽标从内容流的顶部移到底部。

例如，在紧跟包含Livefyre应用程序的元素后，将以下HTML添加到您的页面：

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

然后，将以下内容添加到页面的样式表：

```
/* Hide the top logo */ 
.fyre-widget .fyre-logo-drop, .fyre-widget .fyre-logo-help, .fyre-widget .fyre-help { 
    display:none !important; 
} 
  
/* Style the bottom logo */ 
#powered_by_livefyre_new a {    background: url(https://cdn.livefyre.com/libs/fyre.conv/v3.0.0/images/poweredbylivefyre.png) no-repeat left top; 
    display: block; 
    height: 24px; 
    font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
} 
#powered_by_livefyre_new a:hover { 
    text-decoration: underline; 
}
```

