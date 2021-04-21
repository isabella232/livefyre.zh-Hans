---
description: 通知Livefyre从以前设置的用户同步URL中提取用户信息。 返回布尔值。
title: syncUser网络方法
exl-id: a21ff487-2ab1-4788-b455-84941f03a98f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 5%

---

# syncUser Network Method{#syncuser-network-method}

通知Livefyre从以前设置的用户同步URL中提取用户信息。 返回布尔值。

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| userId | 字符串 | 要与Livefyre同步的用户ID。 在调用此方法之前，必须先与Livefyre设置用户同步URL。 |

## Java示例{#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

示例输出：

```
true
```

## NodeJS示例{#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

示例输出：

```
true
```

## PHP示例{#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

示例输出：

```
true
```

## Python示例{#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

示例输出：

```
True
```

## Ruby示例{#section_enh_gds_rz}

```
network.sync_user(userId) 
```

示例输出：

```
True
```
