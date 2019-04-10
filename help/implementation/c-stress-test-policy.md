---
description: 针对Livefyre平台运行压力测试。
seo-description: 针对Livefyre平台运行压力测试。
seo-title: Stress Test Policy(压力测试政策)
solution: Experience Manager
title: Stress Test Policy(压力测试政策)
uuid: f2d49b55-f4 fc-485f-9aea-a17 ce6413 ee
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Stress Test Policy(压力测试政策){#stress-test-policy}

针对Livefyre平台运行压力测试。

本文档提供针对Livefyre平台运行压力测试的指导。严禁通知客户进行临时测试。有关 [禁止和允许的活动的更多](#c_stress_test_policy/section_mhs_bfz_vdb)信息。

>[!NOTE]
>
>压力测试是可选的。您不需要或希望执行压力测试。Adobe Livefyre作为发布流程的一部分进行常规压力测试和验证。如果您选择运行测试，本文档将概述执行应力测试的要求和限制。

## 通知 {#section_ihs_bfz_vdb}

计划开始时，您必须提前三周或更长时间向Livefyre客户成功专家和Adobe技术顾问通知计划的测试。

要通知Livefyre，请向Livefyre客户成功专家和Adobe技术顾问提交以下信息：

* 目的和测试说明
* 使用的用例是
* 您计划在测试中使用的任何Livefyre API列表
* 测试日期、时间和持续时间
* 用于启动测试的IP地址

## 要求 {#section_khs_bfz_vdb}

您只能在满足以下要求时执行测试：

* 在开始测试之前，您必须获得Adobe技术顾问的明确书面批准或更多信息。
* **您只能在UAT网络上执行测试。**
* 您必须根据真实情况进行测试。例如，您不会假设您的财产每天提供 *数百万* 个帖子请求，因为这并不是一个真实的场景。如果您需要帮助确定您的方案是否真实，请咨询您的Livefyre客户成功专家或Adobe技术顾问。
* 应在太平洋标准时区(UTC-7\)的营业时间内进行测试。
* 您可能需要为测试生成数据和推理。

## 治理 {#section_mhs_bfz_vdb}

Livefyre保留在执行测试时随时终止测试的权利：

* 在生产网络上。
* 未经Adobe技术顾问明确的书面批准，提前三周或更久。
* 应对不切实际的场景。

Livefyre通过阻止访问API、捆绑Livefyre Networks和使用负载测试请求(如果不满足要求)来终止测试。
