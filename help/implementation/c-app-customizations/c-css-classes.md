---
description: 使用可用的CSS类自定义您的应用程序显示。
seo-description: 使用可用的CSS类自定义您的应用程序显示。
seo-title: CSS类
solution: Experience Manager
title: CSS类
uuid: 8714e7e5-3858-458f-a464-de87fd2f0ff0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# CSS类{#css-classes}

使用可用的CSS类自定义您的应用程序显示。

可用于聊天、评论、实时博客、评论和Sidesor。

使用CSS自定义Livefyre应用程序，只需用您自己的样式表覆盖默认的App CSS，即可与页面实现更完整的集成。 本节介绍可用的CSS自定义。

* [编辑器CSS](#c_css_classes/section_edx_prh_xz)
* [排序选项CSS](#c_css_classes/section_btq_4rh_xz)
* [注释CSS](#c_css_classes/section_mlv_nrh_xz)
* [特色评论CSS](#c_css_classes/section_m2v_mrh_xz)
* [存档的注释CSS](#c_css_classes/section_bs5_lrh_xz)
* [注释通知程序CSS](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS类](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## 编辑器CSS {#section_edx_prh_xz}

使用这些类可更改帖子编辑器界面。

| 类 | 描述 |
|---|---|
| .fyre注释计数 | 显示注释数的文本。 |
| .fyre-login-bar | 包含登录栏和选项的定界框。 |
| .fyre-live-container | 围绕听取其头像的人数的定界框。 |
| .fyre编辑器 | .fyre-login-bar、.fyre-live-container周围的定界框以及用户在其中编写注释的文本区域。 |
| .fyre流排序 | 排序选项周围的定界框。 |

您还可以在应用程序配置中编辑样式，包括编辑器字段背景颜色以及编辑器中显示的文本的字体颜色、大小和系列。

要自定义注释编辑器，请将editorCss:{}对象添加到fyre.conv.load()并包含所需的样式。 例如，要使用自定义CSS更新编辑器，请执行以下操作：

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
| .fyre流排序 | 整个排序选项div。 |
| .fyre-stream-sort-newest | 选项“最新”。 |
| .fyre-stream-sort-lost | 选项“最旧”。 |
| .fyre-stream-sort-bar | 选项之间的分隔栏。 |
| .fyre-stream-sort-selected | 当前选择的排序选项。 |

HTML结构：

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

隐藏分隔排序选项的“|”。

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## 注释CSS {#section_mlv_nrh_xz}

| 类 | 描述 |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre将为通过Livefyre的Studio（配置文件同步）添加的每个用户标签创建一个以此格式 [的CSS类](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)。 此类可用于设置用户帐户发布的任何内容（包括该标记）的背景样式。 |
| .fyre-tag-content-icon- *`tag name`* | Livefyre将为通过Livefyre [Studio添加的每个内容标签创建一个此格式的CSS类](/help/implementation/c-app-customizations/c-adding-users-to-groups.md)。 此类可用于设置您向其添加标记的任何内容的样式。 |
| .fyre注释用户 | 包含用户配置文件图片的定界框。 |
| .fyre-comment-username | 用户名。 |
| .fyre版主 | 主持人定界框。 |
| .fyre注释 | 注释文本／链接周围的定界框。 |
| .fyre-comment-article | 整个注释内容的定界框。 |
| .fyre-comment-date | 附加到“发布后的时间”元素的标记。 |
| .fyre-comment-media | 媒体内容周围的定界框。 |
| .fyre注释操作 | 用于对注释执行的可用操作周围的定界框。 |
| .fyre-comment-like | “赞”链接周围的定界框。 |
| .fyre-comment-reply | “回复”链接周围的定界框。 |

## 特色评论CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>所有注释CSS类也可应用于特色内容。

| 类 | 描述 |
|---|---|
| .fyre-featured-content-wrapper | 用于阅读器的容器div。 |
| .fyre-featured-header | 前导标题栏。 |
| .fyre-featured-header-icon | 标题的填充图标。 |
| .fyre-featured-title | 标题文本。 |
| .fyre-feature-body | 读者中特色内容的容器div。 |
| .fyre-featured-quote | 开始每个内容项目的报价图标。 |

## 存档的注释CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>所有内容CSS类也可应用于存档内容。

| 类 | 描述 |
|---|---|
| .fyre-archive-stream-title | “从存档”文本。 |
| .fyre-archive-stream-title-icon | “从存档”标题的标志。 |

## 注释通知程序CSS {#section_dy4_krh_xz}

这些类允许您自定义Livefyre注释通知程序。

| 类 | 描述 |
|---|---|
| .fyre通知 | 列表项（新内容和存档内容）的div。 |
| .fyre通知程序 | 通知程序内容的包装器。 |
| .fyre notifier-archive | 除最新帖子之外的所有新内容的包装器。 |
| .fyre-notifier-avatar | 头像的图像。 |
| .fyre notifier-avatar-container | 用户头像的容器div。 允许您定义定位。 |
| .fyre-notifier-avatar-shading | 头像div的底纹。 |
| .fyre notifier-banner | 通知程序预览内容的容器，用于显示用户头像和最近发布的项目的内容片段。 |
| .fyre-notifier-base | 通知程序信息部分的容器，其中列出新注释的数量、通知程序说明和关闭按钮。 |
| .fyre-notifier-base-close | 通知程序的关闭按钮(x)的容器div。 |
| .fyre notifier-base-shadow | 通知程序基础的底纹。 |
| .fyre notifier-caption | 为通知程序显示的文本。 默认情况下为“新评论”。 |
| .fyre notifier-close | 关闭通知程序的按钮。 |
| .fyre notifier-container | 通知程序的容器包括横幅和基本内容。 |
| .fyre通知程序计数器 | 通知程序中列出的编号的容器。 |
| .fyre notifier-list | 用于最新内容片段的容器。 |
| .fyre notifier-message | 显示内容的前~30个字符。 |
| .fyre notifier-message-container | 标题消息的容器div。 |
