---
description: 实施Livefyre应用程序时，实施的样式取决于您的用例。 本页介绍了创建应用程序的三种方式的功能。
seo-description: 实施Livefyre应用程序时，实施的样式取决于您的用例。 本页介绍了创建应用程序的三种方式的功能。
seo-title: CMS应用程序集成
solution: Experience Manager
title: CMS应用程序集成
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# CMS应用程序集成{#cms-app-integrations}

实施Livefyre应用程序时，实施的样式取决于您的用例。 本页介绍了创建应用程序的三种方式的功能。

Livefyre集成不受任何CMS和用户配置文件以及身份验证平台的限制。 根据您的用例和要求，以一种或多种方式实施Livefyre。

您可以使用传统集成创建自定义的AEM组件。

## CMS应用程序集成类型概述

| 类型 | 开发要求 | 功能 | 优点 | 限制 |
|--- |--- |--- |--- |--- |
| App Designer | 非常低 | 在Studio中创建JS嵌入式文件，以添加到没有开发人员有限样式和可 <br>用配置的页面使用 </br>案例：单次使用页面（活动覆盖、营销活动、枢纽） | 能够在短时间内启动并运行应用程序。 <br>配置可由非技术成员完成。 <br>轻松快速更改配置 | 必须首先使用Livefyre studio创建应用程序不 <br>是自动的 |
| Livefyre.js | 媒介 | 将应用程序集成到页面的JavaScript用 <br>例：可重用模板（编辑内容、产品评论） | 使用整套应用程序自定义和配置自 <br>动化过程，从CMS中将应用程序动态实例化到您的页面 | 需要一个先行的开发人员。 |
| SDK API | 高级 | 从Livefyre检索内容以用于自定义应用程序自定义前端， <br>超越受支持的产品范围自定义 <br>前端用例：数据／分析集成和自定义前端应用程序 | 全面掌控App的外观 | 需要预先开发。 <br>更高级别的开发人员实施工作。 |
