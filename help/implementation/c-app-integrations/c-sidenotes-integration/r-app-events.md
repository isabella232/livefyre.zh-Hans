---
description: 您可以侦听Sidesor实例上的事件。
seo-description: 您可以侦听Sidesor实例上的事件。
seo-title: Sides App Events
solution: Experience Manager
title: Sides App Events
uuid: afca4b03-c370-41ca-aa12-45bc357517ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Sides App Events {#sidenotes-app-events}

您可以侦听Sidesor实例上的事件。

回呼可以注册到该方 `onmethod` 法，也可以不注册该 `removeListener` 方法。 如果 `once` 只调用一次回调，然后取消注册，则方法可方便使用。

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

有关Livefyre事件的详细信息，请参阅“参考”部分中的“JavaScript事件”页。

| 键值 | 描述 |
|--- |--- |
| siserv.initialized | 实例化应用程序时触发，该应用程序包含数据，并且位于页面上。 |
| siestrom.commentFlaged | 标记评论时触发。 数据包含： <br><ul><li>`targetId`:标记为的评论的id</li><li>`type`:标志类型字符串 `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | 在发布评论时触发。 数据包含： <br><ul><li> `authorId`:评论作者的id </li><li>`bodyHtml`:评论正文 </li><li> `parent`:注释的父项的id或null</li></ul> |
| `sidenotes.commentShared` | 共享评论时触发。 数据包含： <br><ul><li>`targetId`:共享的评论的id </li><li> `sharedToFacebook`:评论是否已共享到Facebook </li><li>`sharedToTwitter`:评论是否已共享给Twitter</li></ul> |
| `sidenotes.commentVoted` | 评论投票后被解除。 数据包含： <br><ul><li>`targetId`:投票的评论的id </li><li> `targetAuthorId`:对其评论投票的提交人的id</li><li> `type`:数值投票类型：0:‘clear’, 1:“upvote”，或2:“下调投票”</li></ul> |
| `sidenotes.userLoggedIn` | 用户登录时触发。 数据包含： <br><ul><li>`avatar`:用户的头像URL </li><li>`displayName`:显示用户的名称</li><li>`id`:用户的id</li><li> `isModerator`:用户是否是当前集合的审查方</li></ul> |
| `sidenotes.userLoggedOut` | 用户注销时触发 |
