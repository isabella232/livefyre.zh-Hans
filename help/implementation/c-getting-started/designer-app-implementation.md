---
description: 将Bootstrap和Stream API与Livefyre应用程序结合使用。
seo-description: 将Bootstrap和Stream API与Livefyre应用程序结合使用。
seo-title: 应用程序实施
solution: Experience Manager
title: 应用程序实施
uuid: null
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---

# 应用程序实施 {#appimplementation}

用例：作为客户，我希望使用Livefyre. js方法将Livefyre集成到我的第三方CMS中。

有三种方法可以将Livefyre实施到自定义AEM组件或其他CMS中，如WordPress、SiteCore或Demandware：Designer App实施、API、实施和第三方身份验证集成。

## 设计人员应用程序实施 {#designerapp}

什么：集成Livefyre应用程序最为简单快捷的方法。您可以设计、配置和生成自定义Javascript嵌入代码，以便在几分钟内将LiveFre应用程序集成到页面中。

如何： [创建、预览、发布和嵌入Livefyre应用程序](/help/using/c-about-apps/c-create-an-app.md)

示例： [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Livefyre. js实施 {#livefyrejsimp}

什么： [Livefyre. js](/help/implementation/c-livefyre.js.md) 是支持Apps和Auth网站上的应用程序的核心库。它定义了全局 `window.Livefyre` 对象和一种公共的公共方法Livefyre. needs，它可用于加载其他Livefyre JavaScript库，这些库有助于嵌入Livefyre应用程序并与第三方用户Auth平台集成。

How:

* [使用CollectionMeta令牌创建集合](/help/implementation/t-create-a-collectionmeta-token.md)

* 使用应用程序集成将应用程序集成到第三方CMS

示例：

* 评论应用程序： [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* 评论应用程序： [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* 媒体墙： [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* 有关使用SDK进行高级自定义的信息，请参阅StreamHub SDK。

## API实施 {#apiimplementation}

为了创建自定义体验和数据可视化，使用Bootstrap和Stream API消耗Livefyre和社交数据，可以从头开始创建Livefyre应用程序。

## 第三方身份验证集成 {#thirdpartyauth}

对于需要身份验证的Livefyre应用程序，请参阅 [第三方身份验证平台的身份集成](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) 。

## 客户示例 {#customerexamples}

以下客户通过第三方CMS集成实施Livefyre：

* [PGA Tour Media Wall](https://www.pgatour.com/social-hub.html)

* [Timeout](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
