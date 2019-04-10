---
description: 您可以监听SiteNote实例上的事件。
seo-description: 您可以监听SiteNote实例上的事件。
seo-title: Sidenes App Events
solution: Experience Manager
title: Sidenes App Events
uuid: afca4b03-c370-41ca-aa12-45bc357517 ca
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sidenes App Events {#sidenotes-app-events}

您可以监听SiteNote实例上的事件。

可以使用该方法注册 `onmethod` 和取消注册回调 `removeListener` 。如果回调仅被称为一次，然后取消注册，则可 `once` 方便起见。

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

有关Livefyre事件的详细信息，请参阅“参考”部分中的“JavaScript事件”页面。

| Key | 描述 |
|--- |--- |
| sitenes. initialized | 在实例化应用程序、具有数据并且在页面上时触发。 |
| sitenes. CommentFlaged | 在标记注释时触发。数据包含： <br><ul><li>`targetId`：标记的注释的id</li><li>`type`：标记类型字符串 `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | 在发表评论时触发。数据包含： <br><ul><li> `authorId`：评论作者的id </li><li>`bodyHtml`：评论正文 </li><li> `parent`：注释的父项的id或null</li></ul> |
| `sidenotes.commentShared` | 在共享评论时触发。数据包含： <br><ul><li>`targetId`：共享的注释的id </li><li> `sharedToFacebook`：评论是否共享到Facebook </li><li>`sharedToTwitter`：评论是否共享到Twitter</li></ul> |
| `sidenotes.commentVoted` | 在投票已投票时触发。数据包含： <br><ul><li>`targetId`：已投票的评论的id </li><li> `targetAuthorId`：评论已投票的作者的id</li><li> `type`：数值投票类型：0：“clear”，1：“追加投票”或2：'downloads'</li></ul> |
| `sidenotes.userLoggedIn` | 用户登录时触发。数据包含： <br><ul><li>`avatar`：用户的avatar url </li><li>`displayName`：显示用户的姓名</li><li>`id`：用户ID</li><li> `isModerator`：无论用户是当前集合的主持人</li></ul> |
| `sidenotes.userLoggedOut` | 用户注销时引发 |
