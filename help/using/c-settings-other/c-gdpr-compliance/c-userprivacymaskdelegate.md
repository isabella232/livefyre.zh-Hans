---
description: 您可以更改使用视频蒙版显示的警告文本。
seo-description: 您可以更改使用视频蒙版显示的警告文本。
seo-title: userPrivacyMaskDelegate
solution: Experience Manager
title: userPrivacyMaskDelegate
uuid: e5a2750-bf45-4e70-a5 f9-37f5 e7 c61 f8 e
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

您可以更改使用视频蒙版显示的警告文本。

此文本符合GDPR规定。如果源不支持代理，则Livefyre将在内容上显示此文本和遮罩，除非用户单击视频并批准来自该源的潜在跟踪。

如果您不使用 `userPrivacyMaskDelegate`，将显示以下默认文本：

添加 `userPrivacyMaskDelegate``userPrivacyOptOut`之后。您可以一次性将所有Livefyre隐私标记添加到一个Livefyre对象中。

`userPrivacyMaskDelegate`下面是如何使用的示例：

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
