---
description: 'null'
seo-description: 'null'
seo-title: 将Livefyre与其他Analytics工具一起使用
solution: Experience Manager
title: 将Livefyre与其他Analytics工具一起使用
uuid: 26c835f6-aced-41f7-aabe-418afce8a829
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 将Livefyre与其他Analytics工具一起使用{#use-livefyre-with-other-analytics-tool}

您可以使用分析工具收集与Livefyre Apps用户交互相关的数据。 您可以使用Adobe Analytics或您选择的工具。

要将Livefyre与您选择的工具（而非Adobe Analytics）一起使用，请按照本页中概述的步骤操作。

## 第1步：设置事件处理函数 {#section_ngm_gzl_pdb}

在使用Livefyre应用程序的页面上设置事件处理函数。 这允许您从该页面上的应用程序收集可用于分析的数据。

将Livefyre.js添加到页面以设置事件处理函数。 Livefyre.js异步加载。 为了减小文件大小并提高加载性能，分析不会立即可用。 必须轮询分析对象，直到数据可用。 将此脚本放在页面上的任意位置，或将其捆绑到您自己的编译脚本中。

```
/** 
 * Handler for Livefyre analytics batch events. 
 * @param {Array.<string>} events Array of events that have been fired since 
 * the last batch send. 
 */ 
function analyticsHandler(events) { 
  // Send to analytics 
  console.log(events); 
} 
 
var attempts = 0; 
 
function pollForAnalytics() { 
  if (Livefyre && Livefyre.analytics) { 
    Livefyre.analytics.addHandler(analyticsHandler); 
    return; 
  } 
  if (attempts === 10) { 
    return; 
  } 
  attempts++; 
  setTimeout(pollForAnalytics, 500); 
} 
 
pollForAnalytics(); 
```

## 第2步：实现处理函数

在页面上提供Livefyre.analytics功能后，实施analyticsHandler函数，将收到的事件发送给您选择的分析提供者。

1. 分析处理函数接收一组事件，这些事件必须经过迭代并单独发送，或者作为批次发送（如果提供者支持）。
1. 将处理程序接收的事件数据映射到分析提供者需要的格式。
1. 将数据发送给您的分析提供商。

