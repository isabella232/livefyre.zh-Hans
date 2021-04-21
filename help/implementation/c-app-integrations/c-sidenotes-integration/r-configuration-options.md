---
description: Siestor配置对象是一个JSON对象，用于指定Livefyre应用程序在页面上呈现的内容。
title: 指示配置选项
exl-id: efebf9e5-6623-4953-a8f6-c58495304ac1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---

# Siestrator配置选项{#sidenotes-configuration-options}

Siestor配置对象是一个JSON对象，用于指定Livefyre应用程序在页面上呈现的内容。

该对象包含以下参数：

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| authDelegate | ** requiredobject | 新样式或旧样式已初始化身份验证委托。 |
| collectionMeta | ** requiredobject | 有关详细信息，请参阅collectionMeta令牌。 |
| customIcon | *可选* 字符串 | 设置自定义启动器图标的URL。 默认为Livefyre气泡。 |
| customStyles | *选* 项对象 | 添加自定义样式以更改Sisetr的外观。 有关详细信息，请参阅自定义样式。 |
| disableStream | *可* 选布尔 | 如果为true，则禁用此Siesor实例（而非其他注释流）中的实时流。 默认为 false。 |
| environment（环境） | *可选* 字符串 | 指定Livefyre UAT环境。 唯一可能的值是`t402.livefyre.com`。 对于生产，必须删除此参数。 |
| iconVisibility | *选* 项对象或字符串 | 定义鼠标图标在悬停时还是静态时可见。 如果这是字符串，则它将用于块图标的两个版本（空并且带有Siestr）。 如果是对象，则必须指定每种类型：{empty:&#39;hover&#39;, num:&#39;static&#39;}。 默认为静态。 |
| inlineThreads | *选* 项布尔值 | 如果为true，则Sitexer线程直接插入与其关联的块之后。 默认为 false。 |
| numSiservEl | *选* 项对象、字符串或数组 | 指定Siestor计数构件将装饰的元素。 （此Widget显示页面上的指示数和有关指示符的信息。） 如果字符串选择器匹配多个元素，则将选择第一个元素。 （使用CSS3 DOM选择器规范。） |
| position | *可选* 字符串 | 确定在单击启用了Siser的元素时弹出窗口的位置。 可能的值为“smart”、“left”、“right”、“bottom”。 默认为“smart”，将弹出窗口对齐到页面右侧，除非空间不足（在这种情况下，它将移至内容下方）。 |
| 选择器 | ** requiredobject、string或array | 指定应显示启动器图标的元素。 （使用CSS3 DOM选择器规范。） 如果对象包含“includes”部分和“excludes”部分，该部分将应用CSS选择器以用于任何匹配的包含，并删除与排除匹配的任何元素。 如果为字符串，则页面上将包含任何匹配元素。 如果为数组，则列表要包含的元素。 |
| 字符串 | *选* 项对象 | 添加自定义文本字符串以更改应用程序中的任何语言或文本。 有关详细信息，请参阅自定义字符串。 |
| threadContainerEl | *选* 项对象、字符串或数组 | 指定将显示siestr的线程的元素。 此参数允许您重新确定线程的位置。 如果字符串选择器匹配多个元素，则将选择第一个元素。 （使用CSS3 DOM选择器规范。） |
