---
description: 计算精选的社交项目数。
seo-description: 计算精选的社交项目数。
seo-title: 社交计数器
solution: Experience Manager
title: 社交计数器
uuid: fa aa a1-6a04-4bc1-9bfe-e42 c1250 fd48
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 社交计数器{#social-counter}

计算精选的社交项目数。有关可用端点的完整列表，请参阅“Livefyre [API参考](https://api.livefyre.com/docs) ”部分。

Social Count API可在一段时间内为给定集合中的匹配特选规则返回计数。

>[!NOTE]
>
>此API仅可用于Twitter hashtags。

社交计数器API：

* 资源
* 规则类型
* 响应

## 资源 {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **publiskName：** 您的Livefyre提供了网络名称。For example: *labs* in `labs.fyre.co`.
* **查询：** 所有站点的url-安全base64编码的哈希值，文章ID，规则类型的整数，可为其获取计数信息(预编码)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >查询仅限于10个站点，文章ID，规则类型tuts。(上一个示例将包含个tups。)

* **从**`(optional)` 指定相对或绝对时间段到图形；从指定开始和默认到24小时之前(如果忽略)。
* **直到**`(optional)` 指定图形的相对或绝对时间段；直到指定开始和默认为当前时间(现在)(如果忽略)。

### 相对时间

| Abbreoft | Unit |
|---|---|
| s s | 秒数 |
| 分钟 | 分钟数 |
| h | 小时 |
| d | 天数 |
| w | 周数 |
| mon | 30天(月) |
| y | 365天(年) |

示例：

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## 绝对时间 {#section_xqr_jgc_11b}

格式：HH：MM_ YYYYMMDD

| Abbreoft | 意义 |
|---|---|
| HH | 小时(24h时钟格式) |
| MM | 分钟数 |
| YYYY | 位数年 |
| MM | 月 |
| DD | Day |

示例：

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## 规则类型 {#section_v53_xqb_11b}

| 值 | Type |
|---|---|
| 2 | Twitter |

示例：

要获得网站 `123456` 的最后一分钟计数以及文章ID `some-article-id` 和规则类型， `2`请执行以下操作： `123456:some-article-id;2:`

```
curl -XGET "https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-1min" 
```

示例响应：

```
{ 
    "status": "ok", 
    "code": 200, 
    "data": { 
        "123456": { 
            "some-article-id": { 
                "2": [ 
                    [ 
                        2, 
                        1374770460 
                    ], 
                    [ 
                        4, 
                        1374770470 
                    ], 
                    [ 
                        3, 
                        1374770480 
                    ], 
                    [ 
                        1, 
                        1374770490 
                    ], 
                    [ 
                        0, 
                        1374770500 
                    ], 
                    [ 
                        7, 
                        1374770510 
                    ] 
                ] 
            } 
        } 
    } 
}
```
