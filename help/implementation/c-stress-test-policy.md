---
description: 对Livefyre平台运行压力测试。
seo-description: 对Livefyre平台运行压力测试。
seo-title: 压力测试策略
solution: Experience Manager
title: 压力测试策略
uuid: f2d49b55-f4fc-485f-9aea-a17ce64813ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---


# 压力测试策略{#stress-test-policy}

对Livefyre平台运行压力测试。

本文档提供针对Livefyre平台运行压力测试的指导。 严禁客户在不经通知的情况下进行临时测试。 有关[禁止和允许的活动](#c_stress_test_policy/section_mhs_bfz_vdb)的详细信息。

>[!NOTE]
>
>压力测试是可选的。 您不需要或期望执行压力测试。 AdobeLivefyre在发布过程中进行定期的压力测试和验证。 如果选择运行测试，此文档将概述进行压力测试的要求和限制。

## 通知 {#section_ihs_bfz_vdb}

您必须提前三周或更长时间通知Livefyre客户成功专家和Adobe技术顾问您的计划测试。

要通知Livefyre，请向Livefyre客户成功专家和Adobe技术顾问提交以下信息：

* 测试目的和说明
* 您测试的用例
* 列表您计划在测试中使用的任何Livefyre API
* 测试日期、时间和持续时间
* 启动测试的IP地址

## 要求 {#section_khs_bfz_vdb}

仅当测试符合以下要求时，才能执行测试：

* 在开始测试之前，您必须获得Adobe技术顾问的明确书面批准（3周或更长）。
* **您只能对UAT网络执行测试。**
* 您必须针对真实场景进行测试。 例如，您不能假定您的属性每天为&#x200B;*数百万*&#x200B;帖子请求提供服务，因为这不是现实情况。 如果您需要帮助来确定您的方案是否切合实际，请咨询您的Livefyre客户成功专家或Adobe技术顾问。
* 测试应在工作时间内对Pacific Standard Time Zone \(UTC -7\)进行。
* 您可能需要生成测试数据和推理。

## 管理{#section_mhs_bfz_vdb}

如果您执行测试，Livefyre保留随时终止测试的权利：

* 在生产网络上。
* 未经Adobe技术顾问提前三周或更长时间明确书面批准。
* 面对虚幻的场景。

Livefyre通过阻止对API的访问、禁用Livefyre网络以及拒绝负载测试请求（如果它不符合要求）来终止测试。
