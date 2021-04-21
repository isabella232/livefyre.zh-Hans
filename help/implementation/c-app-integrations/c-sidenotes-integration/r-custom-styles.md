---
description: 自定义样式通过注入到Siser构造函数中的对象应用。
title: 表示自定义样式
exl-id: 846605b7-a21e-4600-bf17-18841d2ed96d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 表示自定样式{#sidenotes-custom-styles}

自定义样式通过注入到Siser构造函数中的对象应用。

&quot;keys&quot;是表示DOM元素的对象键，而&quot;properties&quot;是特定键的CSS属性。 例如，要自定义blockBtn的样式（即启动“显示跨距”的按钮），可以构造如下对象：

```
var styles = { 
   'blockBtn': { 
      'fontColor': '#555', 
      'fontSize': '18px' 
   } 
}; 
new Livefyre.Sidenotes({ 
   customStyles: styles, 
      ...  
})
```

| **键值** | **属性** | 描述 |
|---|---|---|
| `anonymousAvatar` | “height”、“width” | 匿名头像图像，位于文本区域编辑器的左侧。 |
| `blockBtn` | “fontColor”、“fontSize”、“left”、“position”、“right”、“top” | 放在指定为可表示的元素的旁边的“启动器图标”。 |
| `blockBtnActive` | “fontColor”、“fontSize”、“left”、“position”、“right”、“top” | 处于活动状态时的启动器图标。 |
| `commentAvatar` | “height”、“width” | 顶级附注左侧的头像图像。 |
| `commentBody` | “fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“lineHeight” | 串接注释的文本正文。 |
| `commentDisplayName` | “fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“lineHeight” | 显示留有备注的用户的名称。 |
| `commentDownvote` | &#39;fontColor&#39;, &#39;fontSize&#39; | 注释上的“下投”按钮。 |
| `commentReplyExpand` | &quot;backgroundColor&quot;、&quot;borderColor&quot;、&quot;borderWidth&quot;、&quot;fontColor&quot;、&quot;fontFamily&quot;、&quot;fontSize&quot;、&quot;fontWeight&quot;、&quot;lineHeight&quot; | 用于扩展具有大量回复的线程的按钮。 |
| `commentTags` | “fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“lineHeight” | 备注中有关用户的标记。 |
| `commentUpvote` | &#39;fontColor&#39;, &#39;fontSize&#39; | Upvote按钮。 |
| `editorTextarea` | &#39;height&#39;, &#39;width&#39;, &#39;fontColor&#39;, &#39;fontFamily&#39;, &#39;fontSize&#39;, &#39;fontWeight&#39;, &#39;lineHeight&#39; | 用于留言注释的Textarea输入框。 |
| `mediaBlockBtn` | “fontColor”、“fontSize”、“left”、“position”、“right”、“top” | 媒体启动器图标(位于媒体项目（img、视频）顶部时。 |
| `mediaBlockBtnActive` | “fontColor”、“fontSize”、“left”、“position”、“right”、“top” | 处于活动状态的媒体启动器图标。 |
| `numSidenotes` | &#39;fontColor&#39;, &#39;fontFamily&#39;, &#39;fontSize&#39;, &#39;fontWeight&#39;, &#39;lineHeight&#39;, &#39;backgroundColor&#39;, &#39;borderColor&#39;, &#39;borderWidth&#39;, &#39;height&#39;, &#39;width&#39; | 可单击的按钮，显示集合中Siestr的数量。 |
| `numSidenotesPopover` | &#39;fontColor&#39;, &#39;fontFamily&#39;, &#39;fontSize&#39;, &#39;fontWeight&#39;, &#39;lineHeight&#39;, &#39;backgroundColor&#39;, &#39;borderColor&#39;, &#39;borderWidth&#39;, &#39;height&#39;, &#39;width&#39; | 为用户打开快显，并简要说明“Siters”。 |
| `popover` | &#39;backgroundColor&#39; | 调用启动器图标时弹出的跨距。 |
| `popoverArrowLeft` | “backgroundImage”、“height”、“left”、“right”、“top”、“width” | 跨距上指向包含启动器图标的DOM元素的向左箭头元素。 |
| `popoverArrorRight` | “backgroundImage”、“height”、“left”、“right”、“top”、“width” | 跨距上指向包含启动器图标的DOM元素的向右箭头元素。 |
| `popoverArrowTop` | “backgroundImage”、“height”、“left”、“right”、“top”、“width” | 跨距上指向包含启动器图标的DOM元素的顶部箭头元素。 |
| `replyAvatar` | “height”、“width” | 回复级别注释左侧的头像图像。 |
| `streamPoweredBy` | “backgroundColor”、“borderColor”、“lineHeight” | 快显上的“Powered by”页脚。 |
| `streamQueueButton` | &quot;backgroundColor&quot;、&quot;borderColor&quot;、&quot;borderWidth&quot;、&quot;fontColor&quot;、&quot;fontFamily&quot;、&quot;fontSize&quot;、&quot;fontWeight&quot;、&quot;lineHeight&quot; | 用于指示新附注何时流入打开的跨距的按钮。 |
| `userAvatar` | “height”、“width” | 已验证用户的头像图像，位于文本区域编辑器的左侧。 |
