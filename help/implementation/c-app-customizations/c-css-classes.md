---
description: 使用可用的CSS类自定义您的应用程序的显示。
title: CSS类
exl-id: 605f2c47-13f7-4535-90b1-c53cbf548534
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 1%

---

# CSS类{#css-classes}

使用可用的CSS类自定义您的应用程序的显示。

可用于聊天、评论、实时博客、评论和站点。

使用CSS自定义Livefyre应用程序，只需用自己的样式表覆盖默认的App CSS即可实现与页面的更完整集成。 本节介绍可用的CSS自定义。

* [编辑器CSS](#c_css_classes/section_edx_prh_xz)
* [排序选项CSS](#c_css_classes/section_btq_4rh_xz)
* [注释CSS](#c_css_classes/section_mlv_nrh_xz)
* [特色注释CSS](#c_css_classes/section_m2v_mrh_xz)
* [存档的注释CSS](#c_css_classes/section_bs5_lrh_xz)
* [注释通知程序CSS](#c_css_classes/section_dy4_krh_xz)
* [存储CSS类](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## 编辑器CSS {#section_edx_prh_xz}

使用这些类可更改帖子编辑器界面。

| 类 | 描述 |
|---|---|
| .fyre-comment-count | 显示注释数的文本。 |
| .fyre-login-bar | 包含登录栏和选项的边框。 |
| .fyre-live-容器 | 围绕听众和他们的头像的人数的定界框。 |
| .fyre编辑器 | .fyre登录栏、.fyre实时容器和用户编写注释的文本区域周围的定界框。 |
| .fyre-stream-sort | 排序选项周围的定界框。 |

您还可以在应用程序配置中编辑样式，包括编辑器字段背景颜色以及编辑器中显示的文本的字体颜色、大小和系列。

要自定义注释编辑器，请将editorCss:{}对象添加到fyre.conv.load()并包含所需的样式。 例如，要使用自定义CSS更新编辑器：

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
| .fyre-stream-sort | 整个排序选项div。 |
| .fyre-stream-sort-new | 选项“最新”。 |
| .fyre-stream-sort-lost | 选项“最旧”。 |
| .fyre-stream-sort-bar | 选项之间的分隔符栏。 |
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
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre将为通过Livefyre的Studio [用户档案 Sync](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)添加的每个用户标签创建一个采用此格式的CSS类。 此类可用于设置用户帐户发布的任何内容（包括该标记）的背景样式。 |
| .fyre-tag-content-icon- *`tag name`* | Livefyre将为通过Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md)添加的每个内容标签创建一个以此格式的CSS类。 此类可用于设置添加了标记的任何内容的样式。 |
| .fyre-comment-user | 包含用户用户档案图片的边框。 |
| .fyre-comment-username | 用户名。 |
| .fyre-drodma | 主持人定界框。 |
| .fyre-comment | 注释文本/链接周围的定界框。 |
| .fyre-comment-article | 整个注释内容的定界框。 |
| .fyre-comment-date | 附加到“自发布以来的时间”元素的标记。 |
| .fyre-comment-media | 媒体内容周围的定界框。 |
| .fyre-comment-actions | 用于对注释执行的可用操作周围的定界框。 |
| .fyre-comment-like | “喜欢”链接周围的定界框。 |
| .fyre-comment-reply | “回复”链接周围的定界框。 |

## 特色注释CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>所有注释CSS类也可应用于特色内容。

| 类 | 描述 |
|---|---|
| .fyre-featured-content-wrapper | 读取器的容器div。 |
| .fyre-featured-header | 前导标题栏。 |
| .fyre-featured-header-icon | 标题的缩略图标。 |
| .fyre-featured-title | 标题文本。 |
| .fyre-featured-body | 读者中特色内容的容器div。 |
| .fyre-featured-quote | 开始每个内容项目的报价图标。 |

## 存档的注释CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>所有内容CSS类也可以应用于归档内容。

| 类 | 描述 |
|---|---|
| .fyre-archive-stream-title | “从存档”文本。 |
| .fyre-archive-stream-title-icon | “从存档”标题的徽标。 |

## 注释通知程序CSS {#section_dy4_krh_xz}

这些类允许您自定义Livefyre注释通知程序。

| 类 | 描述 |
|---|---|
| .fyre-notification | 列表项（新内容和存档内容）的div。 |
| .fyre notifier | 通告程序内容的包装。 |
| .fyre-notifier-archive | 除最新帖子之外的所有新内容的包装器。 |
| .fyre-notifier-avatar | 头像的图像。 |
| .fyre-notifier-avatar-容器 | 用户头像的容器div。 允许您定义定位。 |
| .fyre-notifier-avatar-shading | 头像div的底纹。 |
| .fyre-notifier-banner | 通知程序预览内容的容器，用于显示用户头像和最近发布的项目的内容片段。 |
| .fyre通告程序库 | 通知程序信息部分的容器，用于列表新注释数、通知程序题注和关闭按钮。 |
| .fyre-notifier-base-close | 通告程序的关闭按钮(x)的容器div。 |
| .fyre-notifier-base-shadow | 通告程序基底的底纹。 |
| .fyre-notifier-caption | 为通知程序显示的文本。 默认情况下为“新建注释”。 |
| .fyre notifier-close | 关闭通知程序的按钮。 |
| .fyre-notifier-容器 | 通知程序的容器包括横幅和基。 |
| .fyre通告程序计数器 | 通知程序中列出的编号的容器。 |
| .fyre-notifier-列表 | 最新内容的容器。 |
| .fyre-notifier-message | 显示内容的前~30个字符。 |
| .fyre-notifier-message-容器 | 标题消息的容器div。 |
