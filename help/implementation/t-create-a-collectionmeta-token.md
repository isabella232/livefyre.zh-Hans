---
description: 通过创建传递到Livefyre的collectionMeta令牌，创建新的集合。
seo-description: 通过创建传递到Livefyre的collectionMeta令牌，创建新的集合。
seo-title: 使用CollectionMeta令牌创建集合
solution: Experience Manager
title: 使用CollectionMeta令牌创建集合
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# 使用CollectionMeta令牌创建集合{#create-a-collection-using-the-collectionmeta-token}

通过创建传递到Livefyre的collectionMeta令牌，创建新的集合。

1. 创建collectionMeta令牌。
1. 创建校验和。

   如果您希望向Livefyre通知您对集合所做的任何更改，则需要校验和。 仅当提供的校验和与先前发送的校验和不同时，Livefyre才会更新您的集合。 创建校验和与创建令牌类似， `collectionMeta` 而不是调用 `buildCollectionMetaToken` 您调用 `buildChecksum`。

创建用户令牌以在Livefyre中进行身份验证。