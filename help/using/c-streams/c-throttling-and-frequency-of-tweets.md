---
description: 并非所有与规则匹配的帖子都显示在流中。
seo-description: 并非所有与规则匹配的帖子都显示在流中。
seo-title: 帖子的限制和频率
solution: Experience Manager
title: 帖子的限制和频率
uuid: b9edfb1e-e6cf-4a48-8756-05f5f18d8799
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# 帖子的限制和频率{#throttling-and-frequency-of-tweets}

并非所有与规则匹配的帖子都显示在流中。

Twitter规则限制和Twitter源中断可以限制流中可见的帖子数。

>[!NOTE]
>
>要确保特定帖子包含在您的流中，请使用“所有资产”页面中的上传资产选项。

* Twitter规则可限制内容，每条规则每5秒提取1条Tweet。 这样，Livefyre应用程序中显示的内容就更加平衡，不会因Tweet而不堪重负。 以这种方式限制传入的帖子还有助于防止流在高通信量期间被淹没或无法读取。

   >[!NOTE]
   >
   >为确保您的高价值作者的内容显示在您的应用程序中，甚至在高速流中，特定作者的规则从不受到限制。

* Twitter源中断可能出于多种原因。 在某些情况下，Twitter不会推送帖子，因此Livefyre不会收到新内容的通知，并且无法显示该内容。 Twitter的API服务中断或大量主题标记／关键字上的流量也可能导致帖子丢失。

