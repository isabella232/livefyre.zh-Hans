---
description: Sidesorp配置对象是一个JSON对象，用于指定Livefyre应用程序在页面上呈现的内容。
seo-description: Sidesorp配置对象是一个JSON对象，用于指定Livefyre应用程序在页面上呈现的内容。
seo-title: Siderap配置选项
solution: Experience Manager
title: Siderap配置选项
uuid: 067e51e6-9720-4226-a805-c7a07c8cdaa0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Siderap配置选项{#sidenotes-configuration-options}

Sidesorp配置对象是一个JSON对象，用于指定Livefyre应用程序在页面上呈现的内容。

该对象包含以下参数：

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| authDelegate | *必需对象* | 新样式或旧样式已初始化身份验证委托。 |
| collectionMeta | *必需对象* | 有关详细信息，请参阅collectionMeta令牌。 |
| customIcon | *可选字符串* | 设置自定义启动器图标的URL。 默认为Livefyre气泡。 |
| customStyles | *可选对象* | 添加自定义样式以更改Sidesk的外观。 有关详细信息，请参阅自定义样式。 |
| disableStream | *可选* Boolean | 如果为true，则禁用此Sidesor实例（而非其他注释流）中的实时流。 默认为 false。 |
| environment（环境） | *可选字符串* | 指定Livefyre UAT环境。 唯一可能的值是 `t402.livefyre.com`。 对于生产，必须删除此参数。 |
| iconVisibility | *可选对象* 或字符串 | 定义鼠标图标在悬停时是可见还是静态时可见。 如果这是字符串，则它将用于块图标的两个版本（空，且带有Sidesk）。 如果是对象，则必须指定每种类型：{empty:“hover”，数字：“static”}。 默认为静态。 |
| inlineThreads | *可选* boolean | 如果为true，则Sitherex线程将直接插入到与其关联的块之后。 默认为 false。 |
| numSidestromEl | *可选对象* 、字符串或数组 | 指定Sidesork计数构件将装饰的元素。 （此构件显示页面上指示的数量和有关指示的信息。）如果字符串选择器与多个元素匹配，则将选择第一个元素。 （使用CSS3 DOM选择器规范。） |
| position | *可选字符串* | 确定在启用了Sidesform的元素被单击时弹出窗口的位置。 可能的值为“smart”、“left”、“right”、“bottom”。 默认为“智能”，该功能将弹出窗口对齐到页面右侧，除非空间不足（在这种情况下，它将移至内容下方）。 |
| 选择器 | *必需的对象* 、字符串或数组 | 指定应显示启动器图标的元素。 （使用CSS3 DOM选择器规范。）如果对象包含“包括”部分和“排除”部分，则这些部分将对任何匹配的包括应用CSS选择器，并删除与排除匹配的任何元素。 如果为字符串，则页面上将包含任何匹配的元素。 如果为数组，则列出要包含的元素。 |
| 字符串 | *可选对象* | 添加自定义文本字符串以更改整个应用程序中的任何语言或文本。 有关详细信息，请参阅自定义字符串。 |
| threadContainerEl | *可选对象* 、字符串或数组 | 指定将显示指示线的元素。 此参数允许您重新定位线程。 如果字符串选择器与多个元素匹配，则将选择第一个元素。 （使用CSS3 DOM选择器规范。） |

