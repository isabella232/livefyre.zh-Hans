---
description: 在服务器上创建一个唯一标记，用于标识您创建的每个集合。
title: CollectionMeta令牌
exl-id: 52edfe75-5ce6-40c9-9afe-c34a3812f1e7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 2%

---

# CollectionMeta Token{#collectionmeta-token}

在服务器上创建一个唯一标记，用于标识您创建的每个集合。

Livefyre为您创建的每个集合分配一个唯一标识符。 Livefyre会分配标题、URL和其他参数，包括：

## collectionMeta Token参数

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| networkName | 字符串（可选） | Livefyre网络的名称（可从[!UICONTROL Studio] > [!UICONTROL Settings] > [!UICONTROL Integration Settings] > [!UICONTROL Credentials]获得）。 当使用库创建collectionMeta令牌时，这是可选的。 |
| networkKey | 字符串（可选） | 特定网络的密钥（可从“Studio”>“设置”>“集成设置”>“凭据”获得）。 当使用库创建collectionMeta令牌时，这是可选的。 |
| siteId | 字符串（可选） | 站点的ID（可从[!UICONTROL Studio > Settings > Integration Settings > Credentials]获得）。 使用库创建collectionMeta令牌时为可选。 |
| siteKey | 字符串（可选） | 站点的密钥（可从[!UICONTROL Studio > Settings > Integration Settings > Credentials]获得）。 |
| articleId | 字符串（可选） | 集合的唯一ID。 |
| title | 字符串（可选） | 要应用于收藏集的标题。 通常，这对应于显示应用程序的页面的标题。 <br>例如：“集成如此有趣！”<br>注意：标题的最大字符长度为255个字符。标题字段不支持HTML实体。 请使用UTF-8对特殊字符进行编码。 |
| url | 字符串（可选） | 要附加到此集合的规范绝对URL。 此URL将用于从Facebook和Twitter上共享的内容、电子邮件通知和Livefyre Studio中生成指向应用程序的链接。 <br>注意：如果在本地进行测试，请使用有效的基本URL域(例如：有效： `https://customer.com`;无效： `https://localhost:5995`)。 |
| 标记 | 字符串（可选） | 单个关键字或短语的逗号分隔列表。 使用Studio按标记搜索集合。  </br>注意：标记不能包含空格。如果您希望在UI中显示空间，请使用下划线。 |
| 扩展 | JSON（可选） | 要传递到集合的JSON格式参数集。 |

## Java {#section_orz_m4n_sz}

```
import com.livefyre.Livefyre; 
import com.livefyre.core.Network; 
import com.livefyre.core.Site; 
import com.livefyre.core.Collection; 
  
Network network = Livefyre.getNetwork("networkName", "networkKey"); 
Site site = network.getSite("siteId", "siteKey"); 
Collection collection = site.buildCommentsCollection("title", "articleId", "https://www.example.com"); 
collection.getData().setTags("tags"); 
  
String collectionMetaToken = collection.buildCollectionMetaToken();
```

## NodeJS {#section_kpk_44n_sz}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork('networkName', 'networkKey'); 
var site = network.getSite('siteId', 'siteKey'); 
var collection = site.buildCommentsCollection('title', 'articleId', 'https://www.example.com'); 
collection.data.tags = 'tags'; 
  
var collectionMetaToken = collection.buildCollectionMetaToken(); 
```

## PHP {#section_zmd_zbj_tz}

```
$network = Livefyre::getNetwork("networkName", "networkKey"); 
$site = $network->getSite("siteId", "siteKey"); 
$collection = $site->buildCommentsCollection("title", "articleId", "https://www.example.com"); 
$collection->getData()->setTags("tags"); 
  
$collectionMetaToken = $collection->buildCollectionMetaToken();
```

## Python {#section_rdm_prj_tz}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token()
```

## 拼音{#section_l5n_qrj_tz}

```
require 'livefyre' 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token 
```

>[!NOTE]
>
>Livefyre接收您构建的collectionMeta令牌，并通过组合siteId（Livefyre提供）和articleId（客户指定）来确定唯一性。
