---
description: Informations Livefyre可从先前设置的用户同步URL中提取用户信息。返回布尔值。
seo-description: Informations Livefyre可从先前设置的用户同步URL中提取用户信息。返回布尔值。
seo-title: SyncUser网络方法
solution: Experience Manager
title: SyncUser网络方法
uuid: Affb03d-3907-4b01-9a64-02ba1b06da14
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# SyncUser网络方法{#syncuser-network-method}

Informations Livefyre可从先前设置的用户同步URL中提取用户信息。返回布尔值。

| 变量 | Type | 描述 |
|--- |--- |--- |
| userID | 字符串 | 要与Livefyre同步的用户ID。在调用此方法之前，必须让用户同步使用Livefyre设置的URL。 |

## Java示例 {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

示例输出：

```
true
```

## NodeJS示例 {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

示例输出：

```
true
```

## PHP示例 {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

示例输出：

```
true
```

## Python示例 {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

示例输出：

```
True
```

## 拼音示例 {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

示例输出：

```
True
```
