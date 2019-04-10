---
description: 从应用程序中删除标准Livefyre应用程序组件。
seo-description: 从应用程序中删除标准Livefyre应用程序组件。
seo-title: 隐藏应用程序元素
solution: Experience Manager
title: 隐藏应用程序元素
uuid: ea090b6e-99f5-4bd7-aa9 e-d39 a4 dff1543
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 隐藏应用程序元素{#hide-app-elements}

从应用程序中删除标准Livefyre应用程序组件。

使用CSS隐藏页面中默认的Livefyre应用程序元素，使您能够自定义用户体验以满足您的需求。

要隐藏应用程序中的元素，只需将显示屏设置为无。

示例：

```
/* Hide the 'reply' button */ 
.fyre-comment-reply { 
    display: none !important; 
} 
  
/* Hide all user avatars */ 
.fyre-comment-user .fyre-mention-item-avatar .fyre-listener-avatars .fyre-avatar fyre-user-avatar-25 { 
    display: none !important; 
} 
.fyre-comment-head .fyre-comment-body .fyre-comment-footer .fyre-comment-divider { 
    margin-left: 0; 
} 
  
/* Hide 'Edit Profile' link */ 
.fyre-edit-profile-link { 
    display: none !important; 
} 
  
/* Hide 'Logout' link */ 
.fyre-logout-link { 
    display: none; 
} 
  
/* Hide 'Comment Notifier' */ 
.fyre-notifier-message { 
    display:none; 
}
```

