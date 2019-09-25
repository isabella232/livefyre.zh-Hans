---
description: 将Bootstrap和流API与Livefyre应用程序结合使用。
seo-description: 将Bootstrap和流API与Livefyre应用程序结合使用。
seo-title: 应用程序实施
solution: Experience Manager
title: 应用程序实施
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1

---

# 应用程序实施 {#appimplementation}

用例：作为客户，我想使用Livefyre.js方法将Livefyre集成到我的第三方CMS中。

在自定义AEM组件或其他CMS（如WordPress、Sitecore或DemandWare）中实施Livefyre有三种方法：设计人员应用程序实施、API、实施和第三方身份验证集成。

## 设计人员应用程序实施 {#designerapp}

什么：集成Livefyre应用程序最简单、最快捷的方法。 您可以设计、配置和生成自定义的Javascript嵌入代码，在几分钟内将LiveFre应用程序集成到页面上。

操作方法：创 [建、预览、发布和嵌入Livefyre应用程序](/help/using/c-about-apps/c-create-an-app.md)

示例： [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Livefyre.js实施 {#livefyrejsimp}

什么：Livefyre [](/help/implementation/c-livefyre.js.md) .js是为站点上的应用程序和身份验证提供支持的核心库。 它定义了全局对象和一个公共方法Livefyre.require，该方法可用于加载其他Livefyre javaScript库，这些库有助于嵌入Livefyre应用程序并与第三方用户身份验证平台集成。 `window.Livefyre`

操作方法：

* [使用CollectionMeta令牌创建集合](/help/implementation/t-create-a-collectionmeta-token.md)

* 使用应用程序集成将应用程序集成到第三方CMS中

示例：

* 评论应用程序： [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* 审阅应用程序： [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* 媒体墙： [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* 有关使用SDK进行高级自定义的信息，请参阅StreamHub SDK。

## API实施 {#apiimplementation}

为了创建自定义的体验和数据可视化，可以使用Bootstrap和Stream API从头开始创建Livefyre应用程序和社交数据。

## 第三方身份验证集成 {#thirdpartyauth}

有关需要身份验证的Livefyre应用程序，请参 [阅适用于第三方身份验证平台的Identity Integration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) 。

## 客户示例 {#customerexamples}

以下客户通过第三方CMS集成实施了Livefyre:

* [PGA巡回媒体墙](https://www.pgatour.com/social-hub.html)

* [超时](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
