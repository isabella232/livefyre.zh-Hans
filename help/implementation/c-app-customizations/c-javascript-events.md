---
description: 可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript 的事件。
title: JavaScript事件定义和示例
exl-id: 5b865974-69aa-4d51-ac26-60f1d8a114fc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 11%

---

# JavaScript事件定义和示例{#javascript-events-definitions-and-examples}

可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript 的事件。

Livefyre提供JavaScript事件，可跟踪Livefyre应用程序中的用户活动。 例如，您可能希望在用户喜欢或共享内容到Twitter或Facebook或发布新内容时更新页面。

Livefyre还允许您向第三方分析集成(Adobe Analytics JS、Google Analytics、动态标签管理等)添加事件，以跟踪应用程序事件。 有关更多信息，请与您的第三方集成管理器合作，以提供正确的事件。

要绑定到这些事件，请在页面上实例化应用程序时向页面添加以下代码。 将事件名替换为`{eventName}`:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('{eventName}', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

>[!NOTE]
>
>为所有事件处理函数提供数据对象。 示例数据对象遵循每个事件。

## commentPosted {#section_qfr_51p_xz}

一位用户发布了评论。

* null的父项是新注释。
* “无”的父项是已编辑的注释。
* 父代的编号是回复的父代ID。

```
data = { 
   authorId: "_u2012@livefyre.com" // The ID of the author of the comment  
   parent: "893549"  
      // The ID of the comment that this new comment is in reply to, else null 
   bodyHtml: "<p>42</>" // The HTML of the submitted Content 
   sharedToFacebook:true // Whether the comment was also posted to Facebook 
   sharedToTwitter:false // Whether the comment was also posted to Twitter 
   title: "demo title" // The title of the review (exists only for Reviews) 
   rating: [90] // Array of ratings for the review (exists only for Reviews) 
} 
```

## commentFlaged {#section_szy_s1p_xz}

用户标记了评论。

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## commentLiked {#section_vc1_r1p_xz}

用户喜欢评论。

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## commentShared {#section_nqb_31p_xz}

用户共享了流中的评论。 (当用户从注释编辑器共享时，此事件不会触发。) 单击“共享”按钮时将触发此事件。

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## commentCountUpdated {#section_qdq_f1p_xz}

此对话中可见注释的总数已更改（递增或递减）。

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## userLoggedIn {#section_yjt_vz4_xz}

用户已登录。

```
data = { 
   avatar: "https://gravatar.com/avatar/50.jpg"  
      // Link to logged in user's avatar image 
   displayName: "NewUser" // Display name of the logged in user 
   id: "newuser@livefyre.com" // ID of the logged in user 
   isModerator:false // Boolean indicating whether logged in user is a moderator 
}
```

## userLoggedOut {#section_tsg_5z4_xz}

用户已注销。

未定义数据。

## social提及{#section_a1w_tz4_xz}

用户在评论中包@mention了一个。 返回以下数组：

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## commentFeatured

审查方用户提供了评论。 返回以下数组：

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

注释流已加载，已从服务器获取初始内容集并向用户显示。

未定义数据。

## showMore {#section_pqg_nz4_xz}

用户单击了&#x200B;**[!UICONTROL Show More]**&#x200B;按钮。

未定义数据。

## userFlowded {#section_xxw_jz4_xz}

当用户单击&#x200B;**[!UICONTROL Follow]**&#x200B;按钮时返回true，当内容发布到流时返回false。

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## userUnflocked {#section_wm1_gz4_xz}

当用户单击&#x200B;**Unfollow**&#x200B;按钮时，返回true；当内容发布到流时，返回false。

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```
