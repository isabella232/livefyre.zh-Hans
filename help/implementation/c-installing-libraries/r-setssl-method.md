---
description: 将API调用的SSL设置为开启或关闭。
seo-description: 将API调用的SSL设置为开启或关闭。
seo-title: setSSL网络方法
solution: Experience Manager
title: setSSL网络方法
uuid: 8d989e63-c859-456a-99ca-8d87933913ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# setSSL网络方法{#setssl-network-method}

将API调用的SSL设置为开启或关闭。

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| ssl | 布尔值 | 默认值为true。 如果希望打开SSL，则为false。 <br><ul><li>True —— 打开SSL </li><li>False —— 关闭SSL</li></ul> |

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

## Ruby示例 {#section_enh_gds_rz}

```
network.ssl = false 
```
