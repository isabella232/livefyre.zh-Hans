---
description: 从应用程序中删除标准Livefyre应用程序组件。
seo-description: 从应用程序中删除标准Livefyre应用程序组件。
seo-title: 隐藏应用程序元素
solution: Experience Manager
title: 隐藏应用程序元素
uuid: ea090b6e-99f5-4bd7-aa9e-d39a4dff1543
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 隐藏应用程序元素{#hide-app-elements}

从应用程序中删除标准Livefyre应用程序组件。

使用CSS在页面中隐藏默认的Livefyre应用程序元素，从而使您能够根据自己的需求自定义用户体验。

要隐藏应用程序中的元素，只需将显示设置为“无”。

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

