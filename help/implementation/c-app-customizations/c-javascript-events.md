---
description: 可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript 的事件。
seo-description: 可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript 的事件。
seo-title: JavaScript事件定义和示例
solution: Experience Manager
title: JavaScript事件定义和示例
uuid: 61da2e2e-8fcd-482d-93df-c946f0475277
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# JavaScript事件定义和示例{#javascript-events-definitions-and-examples}

可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript 的事件。

Livefyre提供JavaScript事件以跟踪Livefyre应用程序中的用户活动。 例如，当用户喜欢或共享内容到Twitter或Facebook，或者发布新内容时，您可能希望更新页面。

Livefyre还允许您将事件添加到第三方分析集成（Adobe Analytics JS、Google Analytics、动态标签管理等）中，以跟踪应用程序事件。 有关详细信息，请与您的第三方集成经理合作以提供正确的事件。

要绑定到这些事件，请在页面上实例化应用程序时，将以下代码添加到页面。 用事件名称替换 `{eventName}`:

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
>为所有事件句柄提供数据对象。 每个事件后面都有数据对象示例。

## commentPosted {#section_qfr_51p_xz}

一位用户发布了评论。

* null的父项是新注释。
* “无”的父项是已编辑的注释。
* 父项的编号是回复的父ID。

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

## commentFlasked {#section_szy_s1p_xz}

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

用户共享了流中的评论。 （当用户从注释编辑器共享时，此事件不会触发。）单击“共享”按钮时将触发此事件。

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

数据未定义。

## socialTuntire {#section_a1w_tz4_xz}

用户在评论中包含@tuntices。 返回以下数组：

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

注释流已加载，并且已从服务器获取初始内容集并显示给用户。

数据未定义。

## showMore {#section_pqg_nz4_xz}

用户单击了该 **[!UICONTROL Show More]** 按钮。

数据未定义。

## userFlowded {#section_xxw_jz4_xz}

当用户单击该按钮时返回 **[!UICONTROL Follow]** true，当内容发布到流时返回false。

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## userUnflowded {#section_wm1_gz4_xz}

当用户单击“取消关注”按 **钮时** ，返回true；当内容发布到流时，返回false。

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```

