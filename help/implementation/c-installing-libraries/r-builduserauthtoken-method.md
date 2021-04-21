---
description: 返回从中调用的网络的已加密用户验证令牌。
title: buildUserAuthToken网络方法
exl-id: dcc61c4b-90d9-42a0-9f46-73a843a4ad78
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 8%

---

# buildUserAuthToken网络方法{#builduserauthtoken-network-method}

返回从中调用的网络的已加密用户验证令牌。

| 变量 | 类型 | 描述 |
|--- |--- |--- |
| userId | 字符串 | 此令牌所属用户的用户ID。 |
| displayName | 字符串 | 用户的显示名称。 |
| 过期 | 双线 | 令牌应在秒后过期。 |

## Java示例{#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## NodeJS示例{#section_xkd_gds_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## PHP示例{#section_ghf_gds_rz}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Python示例{#section_dwg_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Ruby示例{#section_enh_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```
