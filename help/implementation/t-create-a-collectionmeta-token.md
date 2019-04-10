---
description: 通过创建传递给Livefyre的CollectionMeta令牌创建一个新集合。
seo-description: 通过创建传递给Livefyre的CollectionMeta令牌创建一个新集合。
seo-title: 使用CollectionMeta令牌创建集合
solution: Experience Manager
title: 使用CollectionMeta令牌创建集合
uuid: 5e18e8-8568-45bb-9070-d0 fa43 dd819 b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 使用CollectionMeta令牌创建集合{#create-a-collection-using-the-collectionmeta-token}

通过创建传递给Livefyre的CollectionMeta令牌创建一个新集合。

1. 创建collectionMeta令牌。
1. 创建校验和。

   如果您希望向Livefyre通知您对集合所做的任何更改，则需要校验和。仅当提供的校验和与之前发送的校验和不同时，Livefyre才会更新您的收藏集。创建校验和就像创建一个 `collectionMeta` 令牌，而不是调用 `buildCollectionMetaToken` 您调用 `buildChecksum`。

创建用于验证进入Livefyre的用户令牌。