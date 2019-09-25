---
description: 通知Livefyre从先前设置的用户同步URL中提取用户信息。 返回一个布尔值。
seo-description: 通知Livefyre从先前设置的用户同步URL中提取用户信息。 返回一个布尔值。
seo-title: sync用户网络方法
solution: Experience Manager
title: sync用户网络方法
uuid: 2affb03d-3907-4b01-9a64-02ba1b06da14
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# sync用户网络方法{#syncuser-network-method}

通知Livefyre从先前设置的用户同步URL中提取用户信息。 返回一个布尔值。

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| userId | 字符串 | 要与Livefyre同步的用户ID。 在调用此方法之前，必须先与Livefyre设置用户同步URL。 |

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

## Ruby示例 {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

示例输出：

```
True
```
