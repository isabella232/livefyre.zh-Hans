---
description: 自定义样式通过插入到SiteNote构造函数中的对象进行应用。
seo-description: 自定义样式通过插入到SiteNote构造函数中的对象进行应用。
seo-title: Siten表示自定义样式
title: Siten表示自定义样式
uuid: 0f6d7ad6-1f6a-4ed2-b86 a-0d03782 e591 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Siten表示自定义样式{#sidenotes-custom-styles}

自定义样式通过插入到SiteNote构造函数中的对象进行应用。

“键”是表示DOM元素的对象键，而“属性”是特定键的支持CSS属性。例如，要自定义blockBtn的样式(它是启动“SiteNote”弹出窗口的按钮)，系统会构建一个对象，如：

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

| **Key** | **属性** | 描述 |
|---|---|---|
| `anonymousAvatar` | &#39;height&#39;、&#39;width&#39; | 匿名头像图像，在文本区域编辑器的左侧。 |
| `blockBtn` | &#39;fontColor&#39;、&#39;fontSize&#39;、&#39;left&#39;、&#39;position&#39;、&#39;right&#39;、&#39;top&#39; | 位于指定为sitenable的元素旁边的“启动器图标”。 |
| `blockBtnActive` | &#39;fontColor&#39;、&#39;fontSize&#39;、&#39;left&#39;、&#39;position&#39;、&#39;right&#39;、&#39;top&#39; | 处于活动状态时启动器图标。 |
| `commentAvatar` | &#39;height&#39;、&#39;width&#39; | 头像图像位于顶级备注的左侧。 |
| `commentBody` | “fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“LineHeight” | 串接注释的文本正文。 |
| `commentDisplayName` | “fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“LineHeight” | 显示留下备注的用户的姓名。 |
| `commentDownvote` | “fontColor”、“fontSize” | 备注上的“投票”按钮。 |
| `commentReplyExpand` | “backgroundColor”、“borderColor”、“borderWidth”、“fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“LineHeight” | 用于扩展包含大量回复的线程的按钮。 |
| `commentTags` | “fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“LineHeight” | 备注上关于用户的标记。 |
| `commentUpvote` | “fontColor”、“fontSize” | 注释上的“投票”按钮。 |
| `editorTextarea` | &#39;height&#39;、&#39;width&#39;、&#39;fontColor&#39;、&#39;fontFamily&#39;、&#39;fontSize&#39;、&#39;fontWeight&#39;、&#39;LineHeight&#39; | 文本输入框用于离开备注。 |
| `mediaBlockBtn` | &#39;fontColor&#39;、&#39;fontSize&#39;、&#39;left&#39;、&#39;position&#39;、&#39;right&#39;、&#39;top&#39; | 媒体启动器图标(位于媒体项目的顶部，视频)。 |
| `mediaBlockBtnActive` | &#39;fontColor&#39;、&#39;fontSize&#39;、&#39;left&#39;、&#39;position&#39;、&#39;right&#39;、&#39;top&#39; | 处于活动状态的Media启动器图标。 |
| `numSidenotes` | &#39;fontColor&#39;、&#39;fontFamily&#39;、&#39;fontSize&#39;、&#39;fontWeight&#39;、&#39;lineHeight&#39;、&#39;backgroundColor&#39;、&#39;borderColor&#39;、&#39;borderWidth&#39;、&#39;height&#39;、&#39;width&#39; | 可单击按钮，用于显示集合中的席位数。 |
| `numSidenotesPopover` | &#39;fontColor&#39;、&#39;fontFamily&#39;、&#39;fontSize&#39;、&#39;fontWeight&#39;、&#39;lineHeight&#39;、&#39;backgroundColor&#39;、&#39;borderColor&#39;、&#39;borderWidth&#39;、&#39;height&#39;、&#39;width&#39; | 弹出窗口，并简要说明用户的SiteNote。 |
| `popover` | &#39;backgroundColor&#39; | 调用启动器图标时出现的弹出窗口。 |
| `popoverArrowLeft` | &#39;backgroundImage&#39;、&#39;height&#39;、&#39;left&#39;、&#39;right&#39;、&#39;top&#39;、&#39;width&#39; | 弹出窗口上的向左箭头元素，指向包含启动器图标的DOM元素。 |
| `popoverArrorRight` | &#39;backgroundImage&#39;、&#39;height&#39;、&#39;left&#39;、&#39;right&#39;、&#39;top&#39;、&#39;width&#39; | 弹出窗口上的向右箭头元素，指向包含启动器图标的DOM元素。 |
| `popoverArrowTop` | &#39;backgroundImage&#39;、&#39;height&#39;、&#39;left&#39;、&#39;right&#39;、&#39;top&#39;、&#39;width&#39; | 弹出窗口上的顶部箭头元素，指向包含启动器图标的DOM元素。 |
| `replyAvatar` | &#39;height&#39;、&#39;width&#39; | 头像图像位于回复级别备注的左侧。 |
| `streamPoweredBy` | &#39;backgroundColor&#39;、&#39;borderColor&#39;、&#39;LineHeight&#39; | 弹出窗口上的“Powered by”页脚。 |
| `streamQueueButton` | “backgroundColor”、“borderColor”、“borderWidth”、“fontColor”、“fontFamily”、“fontSize”、“fontWeight”、“LineHeight” | 用于在新的备注流进入打开的弹出窗口时指示的按钮。 |
| `userAvatar` | &#39;height&#39;、&#39;width&#39; | 经过身份验证的用户的头像图像，位于文本区域编辑器的左侧。 |

