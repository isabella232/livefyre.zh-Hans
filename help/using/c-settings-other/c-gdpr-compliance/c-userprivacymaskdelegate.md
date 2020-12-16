---
description: 您可以使用更改在视频蒙版上显示的警告文本。
seo-description: 您可以使用更改在视频蒙版上显示的警告文本。
seo-title: userPrivacyMaskDelegate
solution: Experience Manager
title: userPrivacyMaskDelegate
uuid: 8e5a2750-bf45-4e70-a5f9-37f5e7c61f8e
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

您可以使用更改在视频蒙版上显示的警告文本。

本文旨在遵守GDPR规定。 如果源不支持代理，则除非用户单击视频并批准来自该源的潜在跟踪，否则Livefyre会在内容上显示此文本和遮罩。

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
