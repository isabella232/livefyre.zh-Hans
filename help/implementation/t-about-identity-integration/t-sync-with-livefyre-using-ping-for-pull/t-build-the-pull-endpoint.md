---
description: 构建拉取端点，以接收并响应访问您的用户身份系统的请求。
title: 构建拉式端点
exl-id: cc66365b-0d5f-4a0b-954f-ee014e75d4a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# 构建拉式端点{#build-the-pull-endpoint}

构建拉取端点，以接收并响应访问您的用户身份系统的请求。

1. 创建一个HTTPS端点，它接收Livefyre请求并以包含最新用户数据的JSON对象做出响应。

   >[!NOTE]
   >
   >此端点必须可访问。 还强烈建议通过HTTPS协议发送请求和响应。

1. 向Studio注册端点。
