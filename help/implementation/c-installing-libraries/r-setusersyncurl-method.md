---
description: Informations Livefyre将网络用户同步URL更新至提供的URL。返回布尔值。
seo-description: Informations Livefyre将网络用户同步URL更新至提供的URL。返回布尔值。
seo-title: setUserSyncurl网络方法
solution: Experience Manager
title: setUserSyncurl网络方法
uuid: cd067e90-a2 da-4e3 d-8e60-7eabfd86 fc7 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# setUserSyncurl网络方法{#setusersyncurl-network-method}

Informations Livefyre将网络用户同步URL更新至提供的URL。返回布尔值。

| 变量 | Type | 描述 |
|--- |--- |--- |
| URLTemplate | 字符串 | 向Livefyre注册以同步用户ID的URL。需要“`{id}`”作为提供的URL字符串的一部分。 |

## Java示例 {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

示例输出：

```
true
```

## NodeJS示例 {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

示例输出：

```
true
```

## PHP示例 {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

示例输出：

```
true
```

## Python示例 {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

示例输出：

```
True
```

## 拼音示例 {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

示例输出：

```
True
```
