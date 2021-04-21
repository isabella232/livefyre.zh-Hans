---
description: 实施Livefyre应用程序时，实施的样式取决于您的用例。 本页介绍了创建应用程序的三种方式的功能。
title: CMS应用程序集成
exl-id: 7590e247-87cc-470e-bab6-e61a19221dbd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# CMS应用程序集成{#cms-app-integrations}

实施Livefyre应用程序时，实施的样式取决于您的用例。 本页介绍了创建应用程序的三种方式的功能。

Livefyre集成不受任何CMS和用户用户档案及身份验证平台的限制。 根据您的用例和要求，以一种或多种方式实施Livefyre。

您可以使用传统集成创建自定义AEM组件。

## CMS应用程序集成类型概述

| 类型 | 开发要求 | 功能 | 优点 | 限制 |
|--- |--- |--- |--- |--- |
| App Designer | 非常低 | 在Studio中创建JS嵌入式，以添加到没有开发人员<br>可用的有限样式和配置</br>用例的页面：单次使用页面(事件覆盖、活动、集线器) | 能够在短时间内启动并运行应用程序。 <br>配置可由非技术成员完成。<br>轻松快速更改配置 | 必须先使用Livefyre Studio创建应用程序<br>非自动 |
| Livefyre.js | 媒介 | 将应用程序集成到页面的JavaScript中<br>用例：可重复使用的模板（编辑内容、产品评论） | 使用整套应用程序自定义和配置<br>自动化流程，将CMS中的应用程序动态实例化到您的页面 | 需要一名先行开发人员。 |
| SDK API | 高级 | 从Livefyre检索您的内容以用于自定义应用程序<br>自定义前端（不受支持）产品<br>用例：数据/分析集成和自定义前端应用程序 | 完全掌控App的外观 | 需要预先开发。 <br>更高级别的开发人员实施工作。 |
