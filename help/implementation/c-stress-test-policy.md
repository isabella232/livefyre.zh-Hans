---
description: 针对Livefyre平台运行压力测试。
title: 压力测试策略
exl-id: cb87b6ca-4107-46fc-9b1e-dc9399ec6d3a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# 压力测试策略{#stress-test-policy}

针对Livefyre平台运行压力测试。

本文档提供针对Livefyre平台运行压力测试的指导。 严禁客户在未通知的情况下进行临时测试。 有关[禁止的和允许的活动](#c_stress_test_policy/section_mhs_bfz_vdb)的详细信息。

>[!NOTE]
>
>压力测试是可选的。 您不需要或不需要执行压力测试。 Adobe Livefyre在发布过程中定期进行压力测试和验证。 如果选择运行测试，此文档将概述进行压力测试的要求和限制。

## 通知 {#section_ihs_bfz_vdb}

您必须在计划进行开始的三周或三周前通知Livefyre客户成功专家和Adobe技术顾问您的计划测试。

要通知Livefyre，请向Livefyre客户成功专家和Adobe技术顾问提交以下信息：

* 测试的目的和说明
* 您正在测试的用例
* 列表您计划在测试中使用的任何Livefyre API
* 测试的日期、时间和持续时间
* 从中启动测试的IP地址

## 要求 {#section_khs_bfz_vdb}

仅当测试满足以下要求时，才能执行测试：

* 在开始测试之前，您必须获得Adobe技术顾问的明确、书面批准（3周或更长）。
* **您只能对UAT网络执行测试。**
* 您必须根据实际情况进行测试。 例如，您不能假设您的属性每天为&#x200B;*millans*&#x200B;的帖子请求提供服务，因为这不是现实情况。 如果您需要帮助来确定您的方案是否现实，请咨询您的Livefyre客户成功专家或Adobe技术顾问。
* 应在工作时间对太平洋标准时区进行测试\(UTC -7\)。
* 您可能需要生成测试数据和推理。

## 治理{#section_mhs_bfz_vdb}

如果您执行测试，Livefyre保留随时终止测试的权利：

* 在生产网络上。
* 在未明确说明的情况下，提前三周或更长时间获得Adobe技术顾问的书面批准。
* 面对虚幻的场景。

Livefyre通过阻止访问API、禁用Livefyre Networks和拒绝负载测试请求（如果它不满足要求）来终止测试。
