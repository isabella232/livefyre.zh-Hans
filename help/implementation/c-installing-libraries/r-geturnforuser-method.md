---
description: 此方法返回此网络用户的URN。
title: getUrnForUser Network方法
exl-id: 272e724e-d09d-4d7d-9967-a229707ff47f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# getUrnForUser Network Method{#geturnforuser-network-method}

此方法返回此网络用户的URN。

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| userId | 字符串 | 要在URN中使用的userId。 |

## Java示例{#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## NodeJS示例{#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## PHP示例{#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Python示例{#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ruby示例{#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
