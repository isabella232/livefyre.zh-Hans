---
description: 将API调用的SSL设置为打开或关闭。
title: setSSL网络方法
exl-id: 5682b84a-0b4d-479b-af40-60d2c6c38155
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# setSSL网络方法{#setssl-network-method}

将API调用的SSL设置为打开或关闭。

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| ssl | 布尔值 | 默认值为true。 如果希望打开SSL，则为false。<br><ul><li>True — 启用SSL </li><li>False — 关闭SSL</li></ul> |

## Java示例{#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## NodeJS示例{#section_xkd_gds_rz}

```
network.ssl = false; 
```

## PHP示例{#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Python示例{#section_dwg_gds_rz}

```
network.ssl = False 
```

## Ruby示例{#section_enh_gds_rz}

```
network.ssl = false 
```
