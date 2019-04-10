---
description: 为搜索引擎爬虫提供社区内容。
seo-description: 为搜索引擎爬虫提供社区内容。
seo-title: Bootstrap HTML
solution: Experience Manager
title: Bootstrap HTML
uuid: 137e4382-4e7b-4124-9d35-1d872a497bc7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Bootstrap HTML

为搜索引擎爬虫提供社区内容。

有关可用端点的完整列表，请参阅“Livefyre [API参考](https://api.livefyre.com/docs) ”部分。

Livefyre Apps要求您在页面上执行JavaScript以显示集合的内容。由于大多数搜索引擎爬虫无法执行JavaScript，因此他们无法看到社区帖子的内容。使用Bootstrap HTML API将此内容的可搜索片段添加到页面的初始HTTP响应中，从而允许您的内容和关键字改进搜索引擎优化。

>[!NOTE]
>
>此API仅可用于评论和Live Blog Collection类型。

## 集成

Livefyre的Bootstrap HTML API将返回用户内容的HTML片段，该片段可能包含在页面的HTTP响应中。在不执行任何JavaScript的情况下搜索引擎爬虫可读取此响应。页面停留在用户浏览器中后，HTML片段将替换为完整的交互式构件，用户将能够发布内容。

要实施Bootstrap HTML API，请执行以下操作：

1. 向下面记录的Bootstrap HTML端点发出服务器API请求。

   >[!NOTE]
   >
   >如果您正在尝试将Bootstrap HTML用于尚不存在的对话(即您还没有嵌入应用程序或创建集合)，则您将收到200，但内容显示如下： `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. 如果您的退回中没有包含“404”的内容，请将其保存到字符串中。您可以缓存此响应以以后避免在每个页面上请求Bootstrap HTML API。
1. 将Bootstrap HTML字符串插入您希望显示内容的网页。
1. 将网页提供给浏览器(或搜索引擎爬虫)。

## 资源

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## 参数

* **加密名称** 您的Livefyre提供的网络名称。For example: *labs* in `labs.fyre.co`.
* **siteID** 集合的站点ID。
* **b64ArticleID** 使用base64url编码的集合的文章ID。

## 示例

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## 响应

```
https://gist.github.com/ec5c2457322faf9cf515 
```
