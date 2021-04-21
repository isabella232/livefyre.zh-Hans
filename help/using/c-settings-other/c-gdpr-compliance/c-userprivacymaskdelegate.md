---
description: 您可以使用更改在视频蒙版上显示的警告文本。
title: userPrivacyMaskDelegate
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

您可以使用更改在视频蒙版上显示的警告文本。

此文本的存在是为了遵守GDPR规定。 如果源不支持代理，则除非用户单击视频并批准来自该源的潜在跟踪，否则Livefyre会在内容上显示此文本和蒙版。

如果不使用`userPrivacyMaskDelegate`，将显示以下默认文本：

在`userPrivacyOptOut`后添加`userPrivacyMaskDelegate`。 您可以一次添加所有Livefyre隐私标志，作为一个Livefyre对象的一部分。

以下是如何使用`userPrivacyMaskDelegate`的示例：

```
userPrivacyMaskDelegate: function () { 
    var container = document.createElement('div'); 
    var firstParagraph = document.createElement('p'); 
    firstParagraph.innerHTML = 'Text of first paragraph'; 
    var secondParagraph = document.createElement('p'); 
    secondParagraph.innerHTML = 'Text of second paragraph'; 
    container.appendChild(firstParagraph); 
    container.appendChild(secondParagraph); 
    return container; 
}
```
