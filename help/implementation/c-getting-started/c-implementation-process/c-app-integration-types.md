---
description: 实施Livefyre应用程序时，实施的样式取决于您的用例。 本页介绍创建应用程序的三种方法的功能。
seo-description: 实施Livefyre应用程序时，实施的样式取决于您的用例。 本页介绍创建应用程序的三种方法的功能。
seo-title: CMS应用程序集成
solution: Experience Manager
title: CMS应用程序集成
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 1%

---


# CMS应用程序集成{#cms-app-integrations}

实施Livefyre应用程序时，实施的样式取决于您的用例。 本页介绍创建应用程序的三种方法的功能。

Livefyre集成与任何CMS和用户用户档案及身份验证平台无关。 根据您的用例和要求，以一种或多种方式实施Livefyre。

您可以使用传统集成创建自定义AEM组件。

## CMS应用程序集成类型概述

| 类型 | 开发要求 | 功能 | 优点 | 限制 |
|--- |--- |--- |--- |--- |
| App Designer | 非常低 | 在Studio中创建JS嵌入式，以添加到没有开发人员<br>可用的有限样式和配置</br>的页面中：单次使用页面(事件覆盖、活动、集线器) | 能够在短时间内启动并运行应用程序。 <br>配置可由非技术成员完成。<br>轻松快速更改配置 | 必须先使用Livefyre Studio创建应用程序<br>非自动 |
| Livefyre.js | 媒介 | 将应用程序集成到页面<br>的JavaScript中用例：可重用模板（编辑内容、产品评论） | 使用整套应用程序自定义和配置<br>自动化流程，将应用程序从CMS中动态实例化到您的页面 | 需要一名先行的开发人员。 |
| SDK API | 高级 | 从Livefyre检索您的内容以用于自定义应用程序<br>自定义前端（不受支持）产品<br>用例：数据／分析集成和自定义前端应用程序 | 全面掌控App的外观 | 需要预先开发。 <br>更高级别的开发人员实施工作。 |
