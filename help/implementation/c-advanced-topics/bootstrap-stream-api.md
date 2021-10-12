---
description: 将Bootstrap和流API与Livefyre应用程序结合使用。
title: 查看帐户详细信息
exl-id: b8458954-3727-4c4d-93dd-d21a4328e069
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# 将Bootstrap和流API与Livefyre应用程序结合使用 {#bootstrap-stream-api}

## BootstrapAPI {#bootstrap-api}

### 如何检索早于最新50段的内容？ {#howcontentolder}

Bootstrap是Livefyre应用程序中的所有内容。 它是缓存的数据，通常为12到20分钟之前。 它以50块块的形式交付，并进行分页，以便您可以检索50块以上的内容。

[API 参考](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[示例请求](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

上面的示例请求加载`init`页面，该页面包含收藏集设置和约50段最新内容的唯一初始集。 要轮询旧内容，必须加载后续引导页，其中`N`为页码：

请求: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

例如，一个示例应用程序包含120个内容。 内容“1”是最早的内容片段，内容“70”是最新的内容片段。

* `Init` 将以降序方式加载约120-70段内容： [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` 将以升序方式加载~ 1-50段内容：  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json`
* `1.json` 将以升序方式加载~ 51-100个内容：  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json`
* `2.json` 将以升序方式加载约101-120个内容片段：`https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json`

[单击此处查看Bootstrap投票流程图。](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## 流API {#stream-api}

什么是流API?
流是一个较长的轮询，根据设计，流将保持打开状态约30秒。 有关长轮询技术的说明，请访问：[https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

此长轮询端点会将新内容（例如，用户发布评论）、内容状态更改（例如，用户删除其评论、称赞）以及对内容的审核更改（例如，审核者批准某段内容）流传输到Livefyre应用程序。

对流API的请求应为约30秒（长轮询），在30秒后（当中没有新内容流时）会出现预期的超时。

API引用：[https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

示例请求：

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

请注意：流API响应中的`maxEventId`是此响应中更新的最高事件ID。 在构建下一个流API请求的URL时，将此值用作`lastEventId`路径参数，以获取此响应中的所有更新后发生的更新。

以下示例基于评论应用程序：

“第一条评论”是先发布的。 “第二条评论”之后发布。

第一个注释流API响应：

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

响应中的`maxEventId`是“1520289700953369”，将用作`lastEventId`轮询端点，以获取此响应中所有更新之后发生的更新（即“第二条评论”）。

第二个注释流API响应：

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

响应中的`maxEventID` &quot;1520289700953369&quot;反过来应用作`lastEventID`来构建流API响应，以便进行下次更新。
