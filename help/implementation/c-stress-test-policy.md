---
description: Run stress tests against the Livefyre platform.
seo-description: Run stress tests against the Livefyre platform.
seo-title: Stress Test Policy
solution: Experience Manager
title: Stress Test Policy
uuid: f2d49b55-f4fc-485f-9aea-a17ce64813ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Stress Test Policy{#stress-test-policy}

对Livefyre平台运行压力测试。

本文档提供针对Livefyre平台运行压力测试的指导。 严禁客户在不发出通知的情况下进行临时测试。 有关禁止和允 [许的活动的更多信息](#c_stress_test_policy/section_mhs_bfz_vdb)。

>[!NOTE]
>
>压力测试是可选的。 您无需或期望执行压力测试。 Adobe Livefyre在发布过程中会定期进行压力测试和验证。 如果选择运行测试，本文档将概述进行压力测试的要求和限制。

## 通知 {#section_ihs_bfz_vdb}

您必须在计划开始之前三周或三周以上的时间通知Livefyre客户成功专家和Adobe技术顾问您的计划测试。

要通知Livefyre，请向Livefyre客户成功专家和Adobe技术顾问提交以下信息：

* 测试的目的和说明
* 您测试的用例
* 您计划在测试中使用的任何Livefyre API的列表
* 测试的日期、时间和持续时间
* 用于启动测试的IP地址

## 要求 {#section_khs_bfz_vdb}

You may perform tests only if they meet the following requirements:

* 开始测试前，您必须获得Adobe技术顾问的明确书面批准（3周或更久）。
* **You may only perform tests on the UAT Network.**
* 您必须针对真实场景进行测试。 For example, you may not assume that your property will service millions of post requests every day, because this is not a realistic scenario. ** If you need assistance determining whether your scenario is realistic or not, ask your Livefyre Customer Success Specialist or Adobe Technical Consultant.
* Tests should be conducted during business hours for the Pacific Standard Time zone \(UTC -7\).
* You may need to produce data and your reasoning for the test.

## 管理 {#section_mhs_bfz_vdb}

如果您执行测试，Livefyre保留随时终止测试的权利：

* 在生产网络上。
* 未经Adobe技术顾问提前三周或更久的明确书面批准。
* 面对不真实的场景。

Livefyre通过阻止对API的访问、禁用Livefyre网络以及拒绝负载测试请求（如果它不满足要求）来终止测试。
