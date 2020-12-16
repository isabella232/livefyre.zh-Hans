---
description: 返回加密的有效Livefyre令牌，该令牌可用于与其所调用网络的其他Livefyre API进行交互。
seo-description: 返回加密的有效Livefyre令牌，该令牌可用于与其所调用网络的其他Livefyre API进行交互。
seo-title: buildLivefyreToken网络方法
solution: Experience Manager
title: buildLivefyreToken网络方法
uuid: 7c72a05f-669b-4df3-8117-aa4af2f7a179
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# buildLivefyreToken网络方法{#buildlivefyretoken-network-method}

返回加密的有效Livefyre令牌，该令牌可用于与其所调用网络的其他Livefyre API进行交互。

返回加密的有效Livefyre令牌，该令牌可用于与其所调用网络的其他Livefyre API进行交互。

默认情况下，此令牌设置为在其创建后的24小时后过期。

## Java示例{#section_nyl_ycs_rz}

```
network.buildLivefyreToken(); 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## NodeJS示例{#section_xkd_gds_rz}

```
network.buildLivefyreToken(); 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## PHP示例{#section_ghf_gds_rz}

```
network.buildLivefyreToken(); 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Python示例{#section_dwg_gds_rz}

```
network.build_livefyre_token() 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Ruby示例{#section_enh_gds_rz}

```
network.build_livefyre_token() 
```

示例输出：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

