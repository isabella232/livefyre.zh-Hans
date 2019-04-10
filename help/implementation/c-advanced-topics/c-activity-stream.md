---
description: 了解如何监视和存储流经Livefyre系统的用户生成的内容。
seo-description: 了解如何监视和存储流经Livefyre系统的用户生成的内容。
seo-title: 活动流
solution: Experience Manager
title: 活动流
uuid: f40deec1-58ab-41c9-aac4-d2 d8 c9192 bb9
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 活动流 {#activity-stream}

了解如何监视和存储流经Livefyre系统的用户生成的内容。

使用Activity Stream API可使用用户生成的数据，这些数据流经网络或站点上的Livefyre系统。例如：使用此API中的数据根据评级更新搜索索引，或根据客户活动管理用户在第三方系统中的标记。

Activity Stream API：

有关可用端点的完整列表，请参阅“Livefyre API参考”部分。

## 资源 {#section_aql_n4l_b1b}

有两个端点，一个用于模拟环境，另一个用于生产。

### 暂存

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### Production

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### 参数

* **资源：***字符串* 您要为其请求活动数据的对象的URN。

* **自：***整数* 一个64位整数，表示您收到的最后一个事件的ID。如果没有之前的数据，请指定“0”。

## URN字符串 {#section_skl_q4l_b1b}

示例：

* **urn：livefyre：**`example.fyre.co` 活动流 `example.fyre.co`。
* **urn：livefyre：**`example.fyre.co:site=54321``example.fyre.co` 网络下站点54321的活动流。

## 令牌策略 {#section_nwh_c5j_11b}

Activity Stream API使用OAuth Bearer令牌进行身份验证。Beer Tokens是OAuth2.0规范的一部分，在此处正式介绍 [](https://tools.ietf.org/html/rfc6750#section-1.2)。

令牌包含几件事：

* 创建令牌的人。
* 为谁提供了令牌。
* 不再有效的时间。
* 我们正在处理的事情。
* 已授予的权限列表。

### 步骤

创建OAuth Bearer令牌的步骤包括：

* 创建包含颁发者、受众、主题、到期和范围的地图/词典。
* 根据您的机密使用JWT库对JWT令牌进行编码。
* 添加“身份验证：Bearer”。

下面的代码示例演示了Python中的上述步骤：

```
import time 
import jwt 
  
# network data goes here: 
network = "timeout-0.fyre.co" 
network_secret = "...replaceme..." 
  
# api URN 
api_urn = "urn:livefyre:api:core=GetActivityStream" 
  
# expires in 10 seconds 
expiration = int(time.time() + 10) 
  
network_urn = "urn:livefyre:" + network 
  
data = dict(iss=network_urn, aud=network_urn, sub=network_urn, scope=api_urn, exp=expiration) 
  
token = jwt.encode(data, key=network_secret)
```

在此处，看门人令牌键定义为如下所示：

* **s(***isuer)* 具有生成令牌的授权的实体。这可能是Livefyre、站点或网络。(要知道上学迟到，它是您的上级。)
* **ad***(受众)* 生成此令牌的人员。如果您自己创建令牌，则是站点或网络。
* **子***(主题)* 要授予权限的主题。例如，如果要在集合上操作，则主题必须是集合的标识符。(在学校示例的说明中，您是您。)
* **exp***(过期)* 标记不再有效的点。
* **范围***(范围)* 这是在主题上授予的权限列表。“上学迟到”是一个示例。API的名称是另一个示例。

## 示例 {#section_dhl_ytj_11b}

```
curl -H "Authorization: Bearer <BEARER TOKEN>" https://bootstrap.livefyre.com/api/v3.1/activity/?resource=&since=
```

## 响应 {#section_gs2_stj_11b}

```
{ 
"code": 200,  
"data": { 
  "annotations": {},  
  "authors": {  
      /** "a set of every author who generated activity within this window" */ 
      "_up1770425@livefyre.com": { 
        "avatar": "https://gravatar.com/avatar/68c789597150d3e941769a5c0a0c4249/?s=50&d=https://avatars-qa.fyre.co/a/anon/50.jpg",  
        "displayName": "ross_pfahler",   
        "id": "_up1770425@livefyre.com",  
        "profileUrl": "https://www.qa-ext.livefyre.com/profile/1770425/",  
        "tags": [],  
        "type": 1 
      },  
  ... 
  },  
  "collections": {  
      /** "a set of every collection for which an activity was generated" */ 
      "2486601": { 
        "articleIdentifier": "75",  
        "id": "2486601",  
        "site": "290596",  
        "title": "Live Blog",  
        "url": "https://orangesaregreat.com/..." 
      }, 
  ... 
  },  
  /** "the maximum event ID for this window" */ 
  "maxEventId": 1383508243715211, 
  "states": {  
      /** "a set of messages (comments, reviews, etc) for which activity  
           was generated in this window, represents the compiled 
           'state' of the object including visible actions on that object 
           (up-votes, likes, and etc.)" */ 
      "3ad6480eb00c4895b29b7a972380f489@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "annotations": { 
                "rating": [ 90 ], /** "this object is a Rating (4.5)" */ 
                "vote": [ 
                    { 
                      "author": "_up1792695@livefyre.com",  
                      "collectionId": "2486685",  
                      "value": 1 
                    } 
                ] 
              },  
              "attachments": [  
              /** "a list of oembeds; the body of this Rating included  
                  this Youtube video" */ 
                { 
                  "author_name": "mauricio890",  
                  "author_url": "https://www.youtube.com/user/mauricio890",  
                  "height": 480,  
                  "html": "<iframe width=\"854\" height=\"480\" src=\"https://www.youtube.com/embed/pmMAw5a7POU?autoplay=1&feature=oembed\" frameborder=\"0\" allowfullscreen></iframe>",  
                  "link": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "provider_name": "YouTube",  
                  "provider_url": "https://www.youtube.com/",  
                  "thumbnail_height": 360,  
                  "thumbnail_url": "https://i1.ytimg.com/vi/pmMAw5a7POU/hqdefault.jpg",  
                  "thumbnail_width": 480,  
                  "title": "Napoleon Dynamite dance scene",  
                  "type": "video",  
                  "url": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "version": "1.0",  
                  "width": 854 
                } 
              ],  
              // "who authored the content" 
              "authorId": "_up1793160@livefyre.com",  
              "bodyHtml": "<p><strong>Pros:</strong>Boom</p><p><strong>Cons:</strong>Goes</p><p><strong>Description:</strong>The dynamite:</p><p><a href=\"https://www.youtube.com/watch?v=pmMAw5a7POU\" target=\"_blank\" rel=\"nofollow\">https://www.youtube.com/watch?v=pmMAw5a7POU</a><br/></p>",  
              // "UNIX timestamp" 
              "createdAt": 1383257354,  
              "id": "3ad6480eb00c4895b29b7a972380f489@livefyre.com",  
              // "non-empty only if this were a reply" 
              "parentId": "", 
              // "UNIX timestamp"  
              "updatedAt": 1383257356  
          },  
          // "the event ID of this state." 
          "event": 1383369320554187,  
          "lastVis": 3,  
          "source": 0,  
          "type": 0,  
          // "Object visibility: 0 = deleted, 1 = everyone, 2 = bozo,  
          // 3 = owner + admins (e.g. premod)" 
          "vis": 1  
      },  
      "5943789": { 
          "collectionId": "2486688",  
          "content": { 
            "annotations": { 
                // "posted by a moderator" 
                "moderator": true  
            },  
            "authorId": "_up1792872@livefyre.com",  
            "bodyHtml": "<p>This is a regular comment from a moderator</p>",  
            "createdAt": 1383372338,  
            "id": "5943789",  
            "parentId": "",  
            "updatedAt": 1383372338 
          },  
          "event": 1383372338732492,  
          "lastVis": 0,  
          "source": 5,  
          "type": 0,  
          "vis": 1 
      },  
      "863c616a2c0c44239feed0914c282d7c@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "id": "863c616a2c0c44239feed0914c282d7c@livefyre.com" 
          },  
          "event": 1383371303805767,  
          "lastVis": 1,  
          "source": 0,  
          "type": 0,  
          "vis": 0 // "0 = deleted; this object was removed" 
      },  
  ... 
},  
"meta": { 
  // "this describes position in the stream" 
  "cursor": {  
    // "maximum number of objects returned in a single call through this API" 
    "limit": 50,  
    // "the final position in the stream, and from where data should be requested" 
    "next": 1383508243715211, 
    // "the initial position (the 'since' parameter value in this request)" 
    "self": 0  
  } 
},  
"status": "ok" 
} 
```

上次请求后使用新数据的响应：

```
{ 
    "code": 200,  
    "data": { 
        "annotations": {},  
        "authors": {},  
        "collections": {},  
        "maxEventId": -1,  
        "states": {} 
    },  
    "meta": { 
        "cursor": { 
            "limit": 50, 
            /** "indicates there is no data beyond 1383508243715211" */  
            "next": null, 
            "self": 1383508243715211 
        } 
    },  
    "status": "ok" 
}
```

## Notes {#section_hj3_crj_11b}

* 成功调用API将生成HTTP200状态代码。所有其他状态代码都应被视为错误。
* 如果为非null，请将该 `data.meta.cursor.next` 值用作下一请求的 `since` 参数。
* 如果该值为 `data.meta.cursor.next` null，则表示没有要使用的新数据。应稍后重新请求相同 `since` 的值，以查看新数据是否已送达。
* 在实践中，如果值 `data.meta.cursor.next` 为非null，您应立即请求更多数据。
* 在生产中可通过此API获得约两小时的最近数据。
* 您应设置进程以频繁在cron工作时轮询此端点，以避免缺少数据。对于大多数实施，分钟的间隔应该是非常合适的。
