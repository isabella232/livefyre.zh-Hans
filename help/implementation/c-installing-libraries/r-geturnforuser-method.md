---
description: 此方法返回此网络用户的URN。
seo-description: 此方法返回此网络用户的URN。
seo-title: getUrnForUser network方法
solution: Experience Manager
title: getUrnForUser network方法
uuid: b70b8b0f-2b3a-4a1d-90d0-93a97a137ad4
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# getUrnForUser network方法{#geturnforuser-network-method}

此方法返回此网络用户的URN。

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| userId | 字符串 | 要在URN中使用的userId。 |

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

## Ruby示例 {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
