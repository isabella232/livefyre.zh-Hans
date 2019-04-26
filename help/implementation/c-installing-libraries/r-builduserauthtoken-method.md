---
description: 返回从中调用网络的加密用户身份验证令牌。
seo-description: 返回从中调用网络的加密用户身份验证令牌。
seo-title: buildUserToken网络方法
solution: Experience Manager
title: buildUserToken网络方法
uuid: 8828d356-c3 c6-46a6-91bf-83bd59 e35050
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildUserToken网络方法{#builduserauthtoken-network-method}

返回从中调用网络的加密用户身份验证令牌。

| 变量 | Type | 描述 |
|--- |--- |--- |
| userID | 字符串 | 此令牌所属用户的用户ID。 |
| displayName | 字符串 | 用户的显示名称。 |
| 过期 | double | 当令牌应以秒为单位过期时。 |

## Java示例 {#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## NodeJS示例 {#section_xkd_gds_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## PHP示例 {#section_ghf_gds_rz}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Python示例 {#section_dwg_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## 拼音示例 {#section_enh_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```
