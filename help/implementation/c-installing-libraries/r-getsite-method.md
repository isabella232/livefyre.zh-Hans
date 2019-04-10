---
description: 返回新的站点对象。
seo-description: 返回新的站点对象。
seo-title: getSite Network Method
solution: Experience Manager
title: getSite Network Method
uuid: 67de781e-5240-4be5-9e93-c614828 e0 bb5
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# getSite Network Method{#getsite-network-method}

返回新的站点对象。
|变量|类型|说明||
||—||—||—||
| siteID| String|Livefyre为集合所属的网站或应用程序提供的ID。例如：303617。||
| siteKey| String|Livefyre为SiteID提供了机密密钥。|

## Java示例 {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## NodeJS示例 {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## PHP示例 {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Python示例 {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## 拼音示例 {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

