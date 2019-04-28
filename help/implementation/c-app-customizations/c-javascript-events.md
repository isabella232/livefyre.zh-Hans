---
description: 可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript 的事件。
seo-description: 可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript 的事件。
seo-title: JavaScript事件定义和示例
solution: Experience Manager
title: JavaScript事件定义和示例
uuid: 61da2e2e-8fcd-482d-93df-c946 f0457777
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# JavaScript事件定义和示例{#javascript-events-definitions-and-examples}

可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript 的事件。

Livefyre提供JavaScript事件，用于跟踪您的Livefyre应用程序中的用户活动。例如，当用户喜欢或共享内容至Twitter或Facebook或者发布新内容时，您可能希望更新页面。

Livefyre还允许您将事件添加到第三方分析集成(Adobe Analytics JS、Google Analytics、Dynamic Tag Management等)来跟踪App事件。有关更多信息，请与第三方集成管理器一起提供正确的事件。

要绑定到这些事件，请在页面上实例化您的应用程序时将以下代码添加到页面。替换以下活动名称 `{eventName}`：

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
>为所有事件句柄提供数据对象。示例数据对象会跟随每个事件。

## 注释发布 {#section_qfr_51p_xz}

用户发表了评论。

* null的父项是新注释。
* “无”的父项是已编辑的注释。
* 父级的编号是回复的父ID。

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

## 注释标记 {#section_szy_s1p_xz}

用户标记了评论。

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## 评论称赞 {#section_vc1_r1p_xz}

用户喜欢评论。

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## 注释共享 {#section_nqb_31p_xz}

用户共享了流中的评论。(当用户从评论编辑器共享时，此活动不触发。)单击共享按钮时将触发此事件。

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## 注释已过期 {#section_qdq_f1p_xz}

此对话中可见评论的总数已更改(递增或递减)。

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## UserLoggedIn {#section_yjt_vz4_xz}

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

## UserLoggOut {#section_tsg_5z4_xz}

用户已注销。

数据未定义。

## Instancy {#section_a1w_tz4_xz}

用户在评论中包含@提及。返回以下数组：

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## 评论特别推荐

主持人用户介绍了一个评论。返回以下数组：

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

评论流已加载，已从服务器获取初始内容集并显示给用户。

数据未定义。

## Showmore {#section_pqg_nz4_xz}

用户单击了 **[!UICONTROL Show More]** 按钮。

数据未定义。

## Usered {#section_xxw_jz4_xz}

当用户单击 **[!UICONTROL Follow]** 按钮时返回true，将内容发布到流时返回false。

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## UserUned {#section_wm1_gz4_xz}

当用户单击 **“取消关注** ”按钮时返回true，将内容发布到流时返回false。

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```

