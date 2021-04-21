---
description: 返回新的Site对象。
title: getSite网络方法
exl-id: 88782da9-88c6-4e60-9a23-e46d68675d59
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---

# getSite Network Method{#getsite-network-method}

返回新的Site对象。
|变量|类型|描述|
| | | |
|siteId|String|集合所属的网站或应用程序的Livefyre提供的ID。 例如：303617。  |
|siteKey|String|Livefyre为siteId提供的密钥。  |

## Java示例{#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## NodeJS示例{#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## PHP示例{#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Python示例{#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Ruby示例{#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```
