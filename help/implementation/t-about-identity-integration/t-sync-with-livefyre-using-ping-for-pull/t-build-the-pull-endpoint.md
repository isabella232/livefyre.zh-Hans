---
description: 构建拉取端点，以接收并响应访问您的用户标识系统的请求。
seo-description: 构建拉取端点，以接收并响应访问您的用户标识系统的请求。
seo-title: 构建拉取端点
solution: Experience Manager
title: 构建拉取端点
uuid: 1703152f-aaa7-4a88-aa33-d9f8957ad42b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 构建拉取端点{#build-the-pull-endpoint}

构建拉取端点，以接收并响应访问您的用户标识系统的请求。

1. 创建一个HTTPS端点，它接收Livefyre请求并使用包含最新用户数据的JSON对象做出响应。

   >[!NOTE]
   >
   >此端点必须可访问。 还强烈建议通过HTTPS协议发送请求和响应。

1. 使用Studio注册端点。
