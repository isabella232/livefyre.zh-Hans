---
description: 在服务器上创建一个唯一的令牌，用于标识您创建的每个集合。
seo-description: 在服务器上创建一个唯一的令牌，用于标识您创建的每个集合。
seo-title: CollectionMeta令牌
solution: Experience Manager
title: CollectionMeta令牌
uuid: d5db0b0f-2807-4392-874a-94ac3c1e7550
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# CollectionMeta令牌{#collectionmeta-token}

在服务器上创建一个唯一的令牌，用于标识您创建的每个集合。

Livefyre为您创建的每个集合分配唯一标识符。Livefyre分配标题、URL和其他参数，包括：

## CollectionMeta令牌参数

| 参数 | Type | 描述 |
|--- |--- |--- |
| noknName | 字符串(可选) | Livefyre网络的名称(可从{！UICCONTRL Studio&gt;设置&gt;集成设置&gt;凭据])。使用库创建CollectionMeta令牌时，这是可选的。 |
| NetworkKey | 字符串(可选) | 特定网络的秘密密钥(可从“Studio”&gt;“设置”&gt;“集成设置”&gt;“凭据”获取)。使用库创建CollectionMeta令牌时，这是可选的。 |
| SiteID | 字符串(可选) | 站点的ID(可从 [!UICONTROL Studio > Settings > Integration Settings > Credentials] 中获取)。在使用库创建CollectionMeta令牌时可选。 |
| SiteKey | 字符串(可选) | 网站的秘密密钥(可从{！UICCONTRL Studio&gt;设置&gt;集成设置&gt;凭据])。 |
| articleID | 字符串(可选) | 集合的唯一ID。 |
| title | 字符串(可选) | 要应用于集合的标题。通常，这与显示应用程序的页面的标题相对应。<br>例如：“集成如此有趣！”<br>注意：标题的最大字符长度为255个字符。标题字段不支持HTML实体。请使用UTF-8对特殊字符进行编码。 |
| url | 字符串(可选) | 要附加到此集合的规范绝对URL。此URL用于从Facebook和Twitter、电子邮件通知和Livefyre Studio上共享的内容生成回应用程序的链接。<br>注意：如果本地测试，则使用有效的基本URL域(例如：有效： `https://customer.com`；无效： `https://localhost:5995`)。 |
| 标记 | 字符串(可选) | 单个关键字或短语的以逗号分隔的列表。使用Studio按标记搜索集合。</br>注意：标记不能包含空格。如果希望在UI中显示空格，请使用下划线。 |
| 扩展功能 | JSON(可选) | 要传递到集合的JSON格式的参数集。 |

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

## Ruby {#section_l5n_qrj_tz}

```
require 'livefyre' 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token 
```

>[!NOTE] {重要性=“high”}
>
>Livefyre接收您构建的collectionMeta令牌并通过组合SiteID(Livefyre)和ArticleID(指定的客户)来确定唯一性。

