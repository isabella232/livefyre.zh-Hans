---
description: 此方法返回此网络用户的URN。
seo-description: 此方法返回此网络用户的URN。
seo-title: getTurforUser Network方法
solution: Experience Manager
title: getTurforUser Network方法
uuid: b70b8b0f-2b3a-4a1d-90d0-93a97a137ad4
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# getTurforUser Network方法{#geturnforuser-network-method}

此方法返回此网络用户的URN。

| 变量 | Type | 描述 |
|--- |--- |--- |
| userID | 字符串 | 要在URN中使用的userID。 |

## Java示例 {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## NodeJS示例 {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## PHP示例 {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Python示例 {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## 拼音示例 {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```