---
description: 返回新的Site对象。
seo-description: 返回新的Site对象。
seo-title: getSite网络方法
solution: Experience Manager
title: getSite网络方法
uuid: 67de781e-5240-4be5-9e93-c614828e0bb5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# getSite网络方法{#getsite-network-method}

返回新的Site对象。
|变量|类型|描述||—|—|—||siteId|String|Livefyre为集合所属的网站或应用程序提供的ID。 例如：303617。  ||siteKey|String|Livefyre为siteId提供的密钥。  |

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

## Ruby示例 {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

