---
description: 并非所有与规则匹配的推文都显示在流中。
title: Tweets的限制和频率
exl-id: 6b963f8a-1b61-4252-866b-567d7f556aca
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Tweets的限制和频率{#throttling-and-frequency-of-tweets}

并非所有与规则匹配的推文都显示在流中。

Twitter规则限制和Twitter源中断可限制流中可见的帖子数。

>[!NOTE]
>
>要保证您的流中包含特定的帖子，请使用“所有资产”页面中的上传资产选项。

* Twitter规则对内容进行节流，每5秒提取1条推文。 这样，Livefyre应用程序中显示的内容就更加平衡，不会因Tweets而不堪重负。 以这种方式限制传入的推文还有助于防止流在高流量期间被泛洪或无法读取。

   >[!NOTE]
   >
   >为确保您的高价值作者的内容显示在您的应用程序中，甚至在高速流中，特定作者的规则从不受到限制。

* Twitter源中断可能由于几个原因而发生。 在某些情况下，Twitter不会推送帖子，因此Livefyre不会收到有关新内容的通知，因此无法显示该内容。 twitter API的服务中断或大量主题标签/关键字上的流量，也可能导致未能发送的帖子。
