---
description: 计算精选的社交项目数。
seo-description: 计算精选的社交项目数。
seo-title: 社交计数器
solution: Experience Manager
title: 社交计数器
uuid: fa9aa1a8-6a04-4bc1-9bfe-e42c1250fd48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 社交计数器{#social-counter}

计算精选的社交项目数。 有关可用端点的完整列表，请参阅Livefyre [API参考部分](https://api.livefyre.com/docs) 。

Social Counter API会返回给定集合中在一段时间内的间隔内的匹配特选规则计数。

>[!NOTE]
>
>此API仅对Twitter主题标记可用。

社交计数器API:

* 资源
* 规则类型
* 响应

## 资源 {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **** networkName:您的Livefyre提供的网络名称。 例如： *实验室*`labs.fyre.co`。
* **** 查询：URL安全基64编码的散列，包含所有站点、文章ID、应获取其计数信息的规则类型示例（预编码）

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >查询仅限于10个站点、文章ID和规则类型的示例。 （上一个示例将包含3个示例。）

* **from**`(optional)` 指定相对或绝对时间段到图形；from指定开头，如果忽略，则默认为24小时前。
* **直到**`(optional)` 指定图形的相对或绝对时间段；直到指定开始，如果忽略，则默认为当前时间（现在）。

### 相对时间

| 缩写 | 单位 |
|---|---|
| s | 秒 |
| min（分钟） | 分钟 |
| h | 小时 |
| d | 天数 |
| w | 周 |
| mon | 30天（月） |
| y | 365天（年） |

示例：

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## 绝对时间 {#section_xqr_jgc_11b}

格式：HH:MM_YYYYMMDD

| 缩写 | 含义 |
|---|---|
| HH | 小时（24小时时钟格式） |
| MM | 分钟 |
| YYYY | 4位数年份 |
| MM | 月 |
| DD | 日 |

示例：

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## 规则类型 {#section_v53_xqb_11b}

| 值 | 类型 |
|---|---|
| 2 | Twitter |

示例：

要获取站点和文章ID以及规 `123456` 则类型在最 `some-article-id` 后一分钟的计数， `2`例如： `123456:some-article-id;2:`

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
