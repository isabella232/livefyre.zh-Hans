---
description: Siten表示配置对象是一个JSON对象，用于指定Livefyre应用程序在页面上呈现的内容。
seo-description: Siten表示配置对象是一个JSON对象，用于指定Livefyre应用程序在页面上呈现的内容。
seo-title: Sidenes配置选项
solution: Experience Manager
title: Sidenes配置选项
uuid: 067e51e6-9720-4226-a805-c7 a07 c8 cdaa0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Sidenes配置选项{#sidenotes-configuration-options}

Siten表示配置对象是一个JSON对象，用于指定Livefyre应用程序在页面上呈现的内容。

该对象包含以下参数：

| 参数 | Type | 描述 |
|--- |--- |--- |
| authDelegate | *必需* 对象 | 新或旧样式的身份验证委托。 |
| CollectionMeta | *必需* 对象 | 有关详细信息，请参阅collectionMeta令牌。 |
| Customicon | *可选* 字符串 | 设置自定义启动器图标的URL。默认为Livefyre气泡图。 |
| CustomStyles | *可选* 对象 | 添加自定义样式以更改SiteNote的外观。有关更多信息，请参阅自定义样式。 |
| BundleStream | *可选* Boolean | 如果为true，则禁用此SiteNote实例中的实时流(不在其他注释流中)。默认为false。 |
| environment | *可选* 字符串 | 指定Livefyre UAT环境。唯一的可能值 `t402.livefyre.com`是。对于生产，必须删除此参数。 |
| 图标可见性 | *可选* 对象或字符串 | 定义在悬停或静态时SiteNote图标是否可见。如果这是一个字符串，它将用于块图标的两个版本(空和具有SideNote)。如果某个对象，则必须指定每种类型：{空：“hover”，num：&#39;static&#39;}。默认为静态。 |
| inlineReads | *可选* 布尔值 | 如果为true，则将SitenOte线程直接插入与其关联的块之后。默认为false。 |
| NumSiteNotesel | *可选* 对象、字符串或数组 | 指定Siten表示计数构件将装饰的元素。(此构件显示页面上的席位数和有关SidenNote的信息。)如果字符串选择器匹配多个元素，则会选择第一个元素。(使用CSS DOM选择器规范。) |
| position | *可选* 字符串 | 单击启用了Sidenes启用的元素时，确定弹出窗口的位置。可能的值为“smart”、“left”、“right”、“bottom”。默认值为“smart”，它将弹出窗口与页面右侧对齐，除非没有足够的空间(在这种情况下，它将移至内容下方)。 |
| 选择器 | *所需* 的对象、字符串或数组 | 指定应显示启动器图标的元素。(使用CSS DOM选择器规范。)如果对象包括“includes”部分和一个“excludes”部分，该部分将对任何匹配的包括应用CSS选择器，并删除与exclude匹配的任何元素。如果字符串，将在页面中包含任意匹配元素。如果数组，则列出要包含的元素。 |
| strings | *可选* 对象 | 添加自定义文本字符串以更改整个应用程序中的任何语言或文本。有关详细信息，请参阅自定义字符串。 |
| PhotosContainerel | *可选* 对象、字符串或数组 | 指定将显示Sidemote线程的元素。此参数允许您重新定位线程。如果字符串选择器匹配多个元素，则会选择第一个元素。(使用CSS DOM选择器规范。) |

