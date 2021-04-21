---
description: 通过创建传递到Livefyre的collectionMeta令牌，创建新集合。
title: 使用CollectionMeta令牌创建集合
exl-id: d2dafc90-de21-4998-8e85-83f970524329
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 使用CollectionMeta Token{#create-a-collection-using-the-collectionmeta-token}创建集合

通过创建传递到Livefyre的collectionMeta令牌，创建新集合。

1. 创建collectionMeta令牌。
1. 创建校验和。

   如果您希望向Livefyre通知您对您的集合所做的任何更改，则需要校验和。 仅当提供的校验和与之前发送的校验和不同时，Livefyre才会更新您的集合。 创建校验和与创建`collectionMeta`令牌类似，但调用`buildCollectionMetaToken`时调用`buildChecksum`。

创建用户令牌以在Livefyre中进行身份验证。
