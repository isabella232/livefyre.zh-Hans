---
description: 您可以监听Siestr实例上的事件。
seo-description: 您可以监听Siestr实例上的事件。
seo-title: Siestors应用程序事件
solution: Experience Manager
title: Siestors应用程序事件
uuid: afca4b03-c370-41ca-aa12-45bc357517ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# Sidestrap App事件{#sidenotes-app-events}

您可以监听Siestr实例上的事件。

回呼可以注册到`onmethod`，也可以使用`removeListener`方法注册。 如果回调只被调用一次，然后取消注册，则`once`方法便于使用。

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

有关Livefyre事件的详细信息，请参阅“参考”部分中的JavaScript事件页。

| 键值 | 描述 |
|--- |--- |
| sidenotes.initialized | 实例化应用程序时触发，有数据且位于页面上。 |
| sidenotes.commentFlagged | 标记评论时触发。 数据包含：<br><ul><li>`targetId`:已标记注释的id</li><li>`type`:标志类型字符串  `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | 在发布评论时触发。 数据包含：<br><ul><li> `authorId`:评论作者的id </li><li>`bodyHtml`:评论正文 </li><li> `parent`:注释父项的id或null</li></ul> |
| `sidenotes.commentShared` | 共享评论时触发。 数据包含：<br><ul><li>`targetId`:共享的评论的id </li><li> `sharedToFacebook`:评论是否已共享到Facebook </li><li>`sharedToTwitter`:评论是否已共享给Twitter</li></ul> |
| `sidenotes.commentVoted` | 评论投票后被解雇。 数据包含：<br><ul><li>`targetId`:投票的评论的id </li><li> `targetAuthorId`:被投票表决的提交人的id</li><li> `type`:数值投票类型：0:‘clear’, 1:“uppote”或2:“下投”</li></ul> |
| `sidenotes.userLoggedIn` | 用户登录时触发。 数据包含：<br><ul><li>`avatar`:用户的头像url </li><li>`displayName`:显示用户的名称</li><li>`id`:用户的id</li><li> `isModerator`:用户是否是当前集合的审查方</li></ul> |
| `sidenotes.userLoggedOut` | 用户注销时触发 |
