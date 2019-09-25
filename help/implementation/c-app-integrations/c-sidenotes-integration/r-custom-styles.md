---
description: 自定义样式通过注入到Sidesors构造函数中的对象来应用。
seo-description: 自定义样式通过注入到Sidesors构造函数中的对象来应用。
seo-title: 指示自定义样式
title: 指示自定义样式
uuid: 0f6d7ad6-1f6a-4ed2-b86a-0d03782e591e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 指示自定义样式{#sidenotes-custom-styles}

自定义样式通过注入到Sidesors构造函数中的对象来应用。

“键”是表示DOM元素的对象键，而“属性”是特定键的CSS属性。 例如，要自定义blockBtn的样式（即启动Sidesk弹出窗口的按钮），您可以构建如下对象：

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
| `anonymousAvatar` | “height”、“width” | 文本区域编辑器左侧的匿名头像图像。 |
| `blockBtn` | “fontColor”、“fontSize”、“left”、“position”、“right”、“top” | 放在指定为可显示元素旁边的“启动器图标”。 |
| `blockBtnActive` | “fontColor”、“fontSize”、“left”、“position”、“right”、“top” | 处于活动状态时的启动器图标。 |
| `commentAvatar` | “height”、“width” | 顶级附注左侧的头像图像。 |
| `commentBody` | “fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“lineHeight” | 串接附注的文本正文。 |
| `commentDisplayName` | “fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“lineHeight” | 显示留有备注的用户的名称。 |
| `commentDownvote` | “fontColor”、“fontSize” | 注释上的“下投”按钮。 |
| `commentReplyExpand` | “backgroundColor”、“borderColor”、“borderWidth”、“fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“lineHeight” | 用于用大量回复扩展线程的按钮。 |
| `commentTags` | “fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“lineHeight” | 关于备注中用户的标记。 |
| `commentUpvote` | “fontColor”、“fontSize” | 备注上的“上投”按钮。 |
| `editorTextarea` | “height”、“width”、“fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“lineHeight” | 用于留言备注的文本区域输入框。 |
| `mediaBlockBtn` | “fontColor”、“fontSize”、“left”、“position”、“right”、“top” | 媒体启动器图标，位于媒体项目（img、视频）顶部时。 |
| `mediaBlockBtnActive` | “fontColor”、“fontSize”、“left”、“position”、“right”、“top” | 处于活动状态的媒体启动器图标。 |
| `numSidenotes` | “fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“lineHeight”、“backgroundColor”、“borderColor”、“borderWidth”、“height”、“width” | 可单击的按钮，显示集合中指示的字号数。 |
| `numSidenotesPopover` | “fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“lineHeight”、“backgroundColor”、“borderColor”、“borderWidth”、“height”、“width” | 弹出窗口，其中简要说明了用户的“Sides”（大小）。 |
| `popover` | “backgroundColor” | 调用启动器图标时弹出的快显窗口。 |
| `popoverArrowLeft` | “backgroundImage”、“height”、“left”、“right”、“top”、“width” | 弹出窗口上的向左箭头元素，指向包含启动器图标的DOM元素。 |
| `popoverArrorRight` | “backgroundImage”、“height”、“left”、“right”、“top”、“width” | 弹出窗口上的向右箭头元素，指向包含启动器图标的DOM元素。 |
| `popoverArrowTop` | “backgroundImage”、“height”、“left”、“right”、“top”、“width” | 弹出窗口上的顶部箭头元素，指向包含启动器图标的DOM元素。 |
| `replyAvatar` | “height”、“width” | 回复级别注释左侧的头像图像。 |
| `streamPoweredBy` | “backgroundColor”、“borderColor”、“lineHeight” | “Powered by”页脚。 |
| `streamQueueButton` | “backgroundColor”、“borderColor”、“borderWidth”、“fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“lineHeight” | 用于指示新附注何时流入打开的快显窗格的按钮。 |
| `userAvatar` | “height”、“width” | 经过身份验证的用户的头像图像，位于文本区域编辑器的左侧。 |

