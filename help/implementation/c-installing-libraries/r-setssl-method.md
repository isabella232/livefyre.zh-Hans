---
description: 设置用于打开或关闭API调用的SSL。
seo-description: 设置用于打开或关闭API调用的SSL。
seo-title: SitS网络方法
solution: Experience Manager
title: SitS网络方法
uuid: 8d989e63-c859-456a-99ca-8d87933913 ba
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# SitS网络方法{#setssl-network-method}

设置用于打开或关闭API调用的SSL。

| 变量 | Type | 描述 |
|--- |--- |--- |
| SSL | Boolean | 默认为true。如果您希望启用SSL，否则为false。 <br><ul><li>true- SSL上的 </li><li>假- SSL关闭</li></ul> |

## Java示例 {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## NodeJS示例 {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## PHP示例 {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Python示例 {#section_dwg_gds_rz}

```
network.ssl = False 
```

## 拼音示例 {#section_enh_gds_rz}

```
network.ssl = false 
```
