---
description: 通知Livefyre将网络的用户同步URL更新为提供的URL。 返回一个布尔值。
seo-description: 通知Livefyre将网络的用户同步URL更新为提供的URL。 返回一个布尔值。
seo-title: setUserSyncUrl网络方法
solution: Experience Manager
title: setUserSyncUrl网络方法
uuid: cd067e90-a2da-4e3d-8e60-7eabfd86fc7f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# setUserSyncUrl网络方法{#setusersyncurl-network-method}

通知Livefyre将网络的用户同步URL更新为提供的URL。 返回一个布尔值。

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| urlTemplate | 字符串 | 向Livefyre注册以同步用户ID的URL。 要求“`{id}`”作为提供的URL字符串的一部分。 |

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

## Ruby示例 {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

示例输出：

```
True
```
