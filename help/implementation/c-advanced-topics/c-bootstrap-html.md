---
description: 向搜索引擎爬网程序提供社区内容。
title: Bootstrap HTML
exl-id: 22ab4f2d-f433-4805-b0dd-16d4531e425d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---

# Bootstrap HTML

向搜索引擎爬网程序提供社区内容。

有关可用端点的完整列表，请参阅Livefyre [API参考](https://api.livefyre.com/docs)部分。

Livefyre应用程序要求您在页面上执行JavaScript以显示集合的内容。 由于大多数搜索引擎爬虫程序无法执行JavaScript，因此他们无法看到您的社区发布的内容。 使用Bootstrap HTML API将此内容的可搜索片段添加到页面的初始HTTP响应中，从而使您的内容和关键字能够改进搜索引擎优化。

>[!NOTE]
>
>此API仅对“注释”和“实时博客集合”类型可用。

## 集成

Livefyre的Bootstrap HTML API将返回用户内容的HTML片段，该片段可能包含在页面的HTTP响应中。 搜索引擎爬网程序无需执行任何JavaScript即可读取此响应。 页面在用户的浏览器中实时后，HTML片段将替换为完整的交互式构件，用户将能够发布内容。

要实现Bootstrap HTML API，请执行以下操作：

1. 向下面介绍的Bootstrap HTML端点发出服务器到服务器的API请求。

   >[!NOTE]
   >
   >如果您试图为尚不存在的对话（即，如果您尚未嵌入应用程序或创建集合）获取Bootstrap HTML，您将收到200个，但包含的内容类似于：`<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. 如果您的返回不包含其中带有“404”的内容，请将其保存为字符串。 您可以缓存此响应以备以后使用，以避免在每次页面加载时请求Bootstrap HTML API。
1. 将BootstrapHTML字符串插入您希望内容显示的网页。
1. 向浏览器（或搜索引擎爬网程序）提供您的网页。

## 资源

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## 参数

* **网络** 名称您的Livefyre提供的网络名称。例如：`labs.fyre.co`中的&#x200B;*labs*。
* **站** 点ID集合的站点ID。
* **b64articleId** 使用base64url编码的集合的文章ID。

## 示例

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## 响应

```
https://gist.github.com/ec5c2457322faf9cf515 
```
