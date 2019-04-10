---
description: 将Bootstrap和Stream API与Livefyre应用程序结合使用。
seo-description: 将Bootstrap和Stream API与Livefyre应用程序结合使用。
seo-title: 将Bootstrap和Stream API与Livefyre应用程序结合使用
solution: Experience Manager
title: 查看帐户详细信息
uuid: bracce558f-ade8-49d6-abda-9ee754 ce4 ac0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 将Bootstrap和Stream API与Livefyre应用程序结合使用 {#bootstrap-stream-api}

## Bootstrap API {#bootstrap-api}

### 我如何检索比最新50件内容旧的内容？ {#howcontentolder}

Bootstrap是Livefyre App中的所有内容。它是缓存数据，通常为12-20分钟。它以50块的形式提供，分页以便您可以检索50件以上的内容。

[API参考](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[示例请求](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

上面的示例请求加载包含集合设置的 `init` 页面，以及唯一一组~50条最新内容。要对旧内容进行投票，您必须加载后面的Bootstrap页面作为 `N` 页码：

请求： `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

例如，示例应用程序有120个内容。内容“1”是最旧的内容，内容“70”是最新的内容。

* `Init` 将按降序加载~120-70条内容： [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` 将按升序加载~1-50条内容： [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` 将按升序加载~51-100条内容： [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` 将按升序加载~101-120条内容：[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[单击此处可查看Bootstrap投票流程图。](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## Stream API {#stream-api}

什么是Stream API？
流是一个长投票，设计目的是在大约30秒内保持打开状态。有关长民意测验技术的说明，可在以下位置找到： [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

此长轮询端点流新内容(例如，用户发表评论)、内容状态更改(例如，用户将其评论、喜好)和协调更改(例如审核者批准了一段内容)用于Livefyre App。

当没有新的内容流时，对Stream API的请求应为~30秒(长轮询)，并在30秒后超时。

API参考： [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

示例请求：

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

请注意：Stream API响应 `maxEventId` 中的内容是此响应中更新的最高事件ID。在构建下一个Stream API请求的URL时，将此值用作 `lastEventId` 路径参数，以获取此响应中所有更新之后发生的更新。

以下示例基于评论应用程序：

评论“第一个评论”是先发布的。“第二个评论”发布之后。

第一个注释流API响应：

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

响应中的“ `maxEventId` 152028970095369”将用于轮询 `lastEventId` 端点以获取更新(即，第二个注释)在此响应中的所有更新之后发生的。

第二个评论流API响应：

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

响应中 `maxEventID` 的“152028970095369”依次用作为下一个更新构建Stream `lastEventID` API响应。