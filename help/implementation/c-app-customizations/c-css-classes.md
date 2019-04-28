---
description: 使用可用的CSS类自定义应用程序的显示。
seo-description: 使用可用的CSS类自定义应用程序的显示。
seo-title: CSS类
solution: Experience Manager
title: CSS类
uuid: 8714e7e5-3858-458f-a464-de87 fd2 f0 ff0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# CSS类{#css-classes}

使用可用的CSS类自定义应用程序的显示。

可用于聊天、评论、Live Blog、评论和SideNote。

只需使用您自己的样式表覆盖默认的App CSS，使用CSS自定义Livefyre应用程序以与页面更全面地集成。本节介绍可用的CSS自定义。

* [编辑器CSS](#c_css_classes/section_edx_prh_xz)
* [排序选项CSS](#c_css_classes/section_btq_4rh_xz)
* [注释CSS](#c_css_classes/section_mlv_nrh_xz)
* [特色评论CSS](#c_css_classes/section_m2v_mrh_xz)
* [归档的注释CSS](#c_css_classes/section_bs5_lrh_xz)
* [注释通知程序CSS](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS类](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## 编辑器CSS {#section_edx_prh_xz}

使用这些类更改帖子编辑器界面。

| 类 | 描述 |
|---|---|
| . fyre-comment-count | 显示注释数量的文本。 |
| . fyre-login-bar | 包含登录条和选项的定界框。 |
| . fyre-live-container | 用于侦听和他们的avats的人数周围的定界框。 |
| . fyre-editor | . fyre-login-bar、fyre-live-container和用户编写注释的文本区域周围的定界框。 |
| . fyre-stream-sort | 排序选项周围的定界框。 |

您还可以在应用程序配置中编辑样式，包括编辑器字段背景颜色以及编辑器中显示的字体颜色、大小和系列文本。

要自定义注释编辑器，请添加EditorCSS：{} object to fyre. config. load()并包含您所需的样式。例如，要使用自定义CSS更新编辑器：

```
fyre.conv.load(networkConfig, [{ 
   siteId: LF_siteId, 
   el: 'livefyre', 
   articleId: LF_articleId, 
   collectionMeta: #CollectionMeta 
   editorCss: { 
      background: '#ccc', 
      color: 'red', 
      font: '30px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif' 
   } 
}]);
```

## 排序选项CSS {#section_btq_4rh_xz}

| 类 | 描述 |
|---|---|
| . fyre-stream-sort | 整个排序选项div。 |
| . fyre-stream-sort-newest | 选项“Newest”。 |
| . fyre-stream-sort-latest | 选项“Listest”。 |
| . fyre-stream-sort-bar | 选项之间的分隔条。 |
| . fyre-stream-sort-selected | 当前选定的排序选项。 |

HTML结构：

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

隐藏&#39;||“分隔排序选项”。

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## 注释CSS {#section_mlv_nrh_xz}

| 类 | 描述 |
|---|---|
| . fyre-comment-author-tag- *`custom tag name`* | Livefyre将为通过Livefyre的Studio、 [Profile Sync添加的每个用户标签创建一个采用此格式的CSS类](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)。此类可用于为包括该标记在内的用户帐户发布的任何内容设置背景样式。 |
| . fyre-tag-content-icon- *`tag name`* | Livefyre将为通过Livefyre [Studio添加的每个内容标记创建此格式的CSS类](/help/implementation/c-app-customizations/c-adding-users-to-groups.md)。此类可用于设置您添加标记的任何内容的样式。 |
| . fyre-comment-user | 包含用户配置文件图片的定界框。 |
| . fyre-comment-username | 用户名。 |
| . fyre-审核者 | 主持人定界框。 |
| . fyre-comment | 注释文本/链接周围的定界框。 |
| . fyre-comment-article | 整个评论内容的定界框。 |
| . fyre-comment-date | 附加到“之后time”元素的标记。 |
| . fyre-comment-media | 媒体内容周围的边框。 |
| . fyre-comment-actions | 可用操作周围的边框，用于添加注释。 |
| . fyre-comment-like | “赞”链接周围的定界框。 |
| . fyre-comment-response | “回复”链接周围的定界框。 |

## 特色评论CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>所有注释CSS类也可能应用于特色内容。

| 类 | 描述 |
|---|---|
| . fyre-professional-content-dogper | 供读者使用的容器div。 |
| . fyre-professional-header | 领先的标题栏。 |
| . fyre-professional-header-icon | 标题的quale图标。 |
| . fyre-professional-title | 标题文本。 |
| . fyre-professional-body | reader中特色内容的容器div。 |
| . fyre-professional-quote | 开始每个内容项目的报价图标。 |

## 归档的注释CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>所有内容CSS类也可能应用于存档的内容。

| 类 | 描述 |
|---|---|
| . fyre-archive-stream-title | “From the Archive”文本。 |
| . fyre-archive-stream-title-icon | “From the Archive”标题的徽标。 |

## 注释通知程序CSS {#section_dy4_krh_xz}

这些类允许您自定义Livefyre注释通知程序。

| 类 | 描述 |
|---|---|
| . fyre-Notification | 列表项的div(新内容和归档内容)。 |
| . fyre-notifier | 通知程序内容的包装器。 |
| . fyre-notifier-archive | 除最新帖子之外的所有新内容的包装器。 |
| . fyre-notifier-avatar | 头像的图像。 |
| . fyre-notifier-avatar-container | 用户头像的容器div。允许您定义定位。 |
| . fyre-notifier-avatar-shading | avatar div的阴影。 |
| . fyre-notifier-banner | 通知程序预览内容的容器，用于显示用户头像和最近发布的项目的内容片段。 |
| . fyre-notifier-base | 通知程序信息部分的容器，它列出了新注释、通知程序题注和关闭按钮的数量。 |
| . fyre-notifier-base-close | 通知程序的关闭按钮(x)的容器div。 |
| . fyre-notifier-base-shadow | 通知基础的阴影。 |
| . fyre-notifier-caption | 通知程序显示的文本。默认情况下，“新建评论”。 |
| . fyre-notifier-close | 关闭通知程序的按钮。 |
| . fyre-notifier-container | 通知程序的容器包括横幅和基础。 |
| . fyre-notifier-count | 通知程序中列出的数字的容器。 |
| . fyre-notifier-list | 最新内容的容器。 |
| . fyre-notifier-message | 显示的内容前~30个字符。 |
| . fyre-notifier-message-container | 标题消息的容器div。 |
