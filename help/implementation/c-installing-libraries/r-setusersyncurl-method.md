---
description: 通知Livefyre将网络的用户同步URL更新到提供的URL。 返回布尔值。
title: setUserSyncUrl网络方法
exl-id: 8124ac0f-013f-4943-a33c-6cf8fe696f95
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# setUserSyncUrl网络方法{#setusersyncurl-network-method}

通知Livefyre将网络的用户同步URL更新到提供的URL。 返回布尔值。

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| urlTemplate | 字符串 | 要向Livefyre注册以同步用户ID的URL。 要求“`{id}`”作为提供的URL字符串的一部分。 |

## Java示例{#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

示例输出：

```
true
```

## NodeJS示例{#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

示例输出：

```
true
```

## PHP示例{#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

示例输出：

```
true
```

## Python示例{#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

示例输出：

```
True
```

## Ruby示例{#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

示例输出：

```
True
```
