---
description: 构建提取端点以接收和响应访问用户身份系统的请求。
seo-description: 构建提取端点以接收和响应访问用户身份系统的请求。
seo-title: 构建拖动端点
solution: Experience Manager
title: 构建拖动端点
uuid: 1703152f-aa7-4a88-aa33-d9 f8957 ad42 b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 构建拖动端点{#build-the-pull-endpoint}

构建提取端点以接收和响应访问用户身份系统的请求。

1. 创建一个HTTPS端点，它接收Livefyre请求并对包含最新用户数据的JSON对象做出响应。

   >[!NOTE]
   >
   >必须可访问此端点。强烈建议通过HTTPS协议发送请求和响应。

1. 使用Studio注册端点。
