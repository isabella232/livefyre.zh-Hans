---
description: 了解如何监视和存储流经Livefyre系统的用户生成内容。
seo-description: 了解如何监视和存储流经Livefyre系统的用户生成内容。
seo-title: 活动流
solution: Experience Manager
title: 活动流
uuid: f40deec1-58ab-41c9-aac4-d2d8c9192bb9
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---


# 活动流{#activity-stream}

了解如何监视和存储流经Livefyre系统的用户生成内容。

使用活动流API消费流经网络或站点上Livefyre系统的用户生成的数据。 例如：使用来自此API的数据根据评级更新搜索索引，或根据用户的活动管理第三方系统中的用户徽章。

活动流API:

有关可用端点的完整列表，请参阅Livefyre API参考部分。

## 资源 {#section_aql_n4l_b1b}

有两个端点，一个用于暂存环境，另一个用于生产。

### 暂存

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### 生产

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### 参数

* **resource:** ** string您请求活动数据的对象的URN。

* **since:** ** integer表示您收到的上一个事件的ID的64位整数。如果您没有先前的数据，请指定“0”。

## URN字符串{#section_skl_q4l_b1b}

示例：

* **urn:livefyre:** `example.fyre.co` 的活动流 `example.fyre.co`。
* **urn:livefyre：网** `example.fyre.co:site=54321` 络下站点54321的活动 `example.fyre.co` 流。

## 令牌策略{#section_nwh_c5j_11b}

活动流API使用OAuth承载令牌进行身份验证。 承载令牌是OAuth 2.0规范的一部分，并正式在此[](https://tools.ietf.org/html/rfc6750#section-1.2)中进行了说明。

代号包含以下几项：

* 创建令牌的人。
* 谁被赋予了代号。
* 它不再有效的时间。
* 我们在做的事。
* 已授予的列表权限。

### 步骤

创建OAuth载体令牌的步骤包括：

* 创建包含发行者、受众、主题、到期和范围的地图／字典。
* 将JWT库与您的机密一起使用，对JWT令牌进行编码。
* 添加“身份验证：承载”。

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

其中，如下定义了承载令牌密钥：

* **is** *（颁发者）* 有权生成令牌的实体。这可能是Livefyre、站点或网络。 （如果要提前上学，您的父母应该提醒您。）
* **aud** *(受众* )生成此令牌的人。如果您自己创建的令牌是站点或网络。
* **子** *(主* 题)要授予权限的主题。例如，如果您正在对集合进行操作，则主题必须是集合的标识符。 （在学校示例的备注中，它是您。）
* **exp** *(Expiration)* 令牌不再有效的时间点。
* **范围** *(范* 围)这是对主题授予的权限的列表。“上学迟到”就是一个例子。 API的名称是另一个示例。

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

自上次请求以来具有新数据的响应：

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

## 注释 {#section_hj3_crj_11b}

* 成功调用API将生成HTTP 200状态代码。 所有其他状态代码都应被视为错误。
* 如果为非null，请将`data.meta.cursor.next`中的值用作下一个请求的`since`参数。
* 如果`data.meta.cursor.next`的值为null，则表示没有要使用的新数据。 您以后应使用相同的`since`值重新请求，以查看新数据是否已到达。
* 实际上，如果`data.meta.cursor.next`值为非空，您应立即请求更多数据。
* 通过此API在生产中可获得大约两个小时的最新数据。
* 您应设置进程以在cronjob上频繁轮询此端点，以避免丢失数据。 对于大多数实施，间隔为5分钟应完全足够。
