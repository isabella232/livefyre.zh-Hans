---
description: 您可以侦听Siserv实例上的事件。
title: Siestors应用程序事件
exl-id: e341ca76-002d-425c-8d1a-35c3253fb254
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Siestors应用程序事件{#sidenotes-app-events}

您可以侦听Siserv实例上的事件。

回调可以注册到`onmethod`，并使用`removeListener`方法取消注册。 `once`方法为方便起见，如果只调用一次回调，然后取消注册。

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

有关Livefyre事件的详细信息，请参阅“参考”部分中的JavaScript事件页。

| 键值 | 描述 |
|--- |--- |
| sidenotes.initialized | 实例化应用程序时触发，包含数据，且位于页面上。 |
| sidenotes.commentFlagged | 在标记评论时触发。 数据包含：<br><ul><li>`targetId`:已标记的注释的id</li><li>`type`:标志类型字符串  `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | 在发布评论时触发。 数据包含：<br><ul><li> `authorId`:评论作者的id </li><li>`bodyHtml`:评论正文 </li><li> `parent`:注释父项的id或null</li></ul> |
| `sidenotes.commentShared` | 共享评论时触发。 数据包含：<br><ul><li>`targetId`:共享的评论的id </li><li> `sharedToFacebook`:评论是否已分享给Facebook </li><li>`sharedToTwitter`:评论是否已分享给Twitter</li></ul> |
| `sidenotes.commentVoted` | 在对评论投票后被解聘。 数据包含：<br><ul><li>`targetId`:投票的评论的id </li><li> `targetAuthorId`:对其评论投票的提交人的id</li><li> `type`:数值投票类型：0:&#39;clear&#39;, 1:“upvote”或2:“downvote”</li></ul> |
| `sidenotes.userLoggedIn` | 用户登录时触发。 数据包含：<br><ul><li>`avatar`:用户的avatar url </li><li>`displayName`:用户的显示名称</li><li>`id`:用户的id</li><li> `isModerator`:用户是否是当前集合的审查方</li></ul> |
| `sidenotes.userLoggedOut` | 用户注销时触发 |
