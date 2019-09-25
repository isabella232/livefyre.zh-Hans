---
description: 将Bootstrap和流API与Livefyre应用程序结合使用。
seo-description: 将Bootstrap和流API与Livefyre应用程序结合使用。
seo-title: 将Bootstrap和流API与Livefyre应用程序结合使用
solution: Experience Manager
title: 查看帐户详细信息
uuid: bace558f-ade8-49d6-abda-9ee754ce4ac0
translation-type: tm+mt
source-git-commit: d615705ccf5e4511cc735ce91d95c3e15d0c0160

---


# 将Bootstrap和流API与Livefyre应用程序结合使用 {#bootstrap-stream-api}

## Bootstrap API {#bootstrap-api}

### 如何检索早于最新50个部分的内容？ {#howcontentolder}

Bootstrap是Livefyre应用程序中的所有内容。 它是缓存的数据，通常为12-20分钟。 它以50个块的形式提供，并分页，因此您可以检索50个以上的内容。

[API 参考](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[示例请求](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

上面的示例请求加载包 `init` 含“集合设置”和仅包含约50个最新内容的初始集合的页面。 要轮询旧内容，您必须加载后续引导页面， `N` 并且页码为：

请求: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

例如，一个范例应用程序包含120个内容。 内容“1”是最旧的内容，内容“70”是最新的内容。

* `Init` 将以降序加载~120-70段内容： [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` 将按升序加载~ 1-50个内容： [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` 将按升序加载~ 51-100个内容： [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` 将按升序加载~101-120段内容：[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[单击此处查看Bootstrap投票流程图。](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## 流API {#stream-api}

什么是Stream API?
流是一项长投票，根据设计，它可保持30秒左右的打开时间。 有关长轮询技术的说明，请访问： [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

此长轮询端点将新内容（例如，用户发布评论）、内容状态更改（例如，用户删除其评论、喜欢）和对内容的审核更改（例如，审查方批准某段内容）流式传送到Livefyre应用程序。

对流API的请求应为~30秒（长轮询），当没有新内容流进入时，在30秒后会出现预期超时。

API参考： [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

示例请求：

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

请注意：流 `maxEventId` API响应中的事件ID是此响应中更新的最高事件ID。 在构建您的下 `lastEventId` 一个流API请求的URL时，将此值用作路径参数，以获取此响应中的所有更新后发生的更新。

以下示例基于评论应用程序：

“第一条评论”是先发布的。 “第二条评论”随后发布。

第一个注释流API响应：

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

响 `maxEventId``lastEventId` 应中为“1520289700953369”，将用于轮询端点以获取在响应中的所有更新之后发生的更新（即“第二条评论”）。

第二个注释流API响应：

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

响 `maxEventID` 应中的“1520289700953369”应用作构建流API响应以用于下次更 `lastEventID` 新。