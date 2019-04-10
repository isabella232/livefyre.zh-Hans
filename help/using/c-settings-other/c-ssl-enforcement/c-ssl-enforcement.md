---
description: null
seo-description: null
seo-title: SSL执行
solution: Experience Manager
title: SSL执行
uuid: e64af8c2-3ab6-4034-b385-0e552 d828 c6 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# SSL执行{#ssl-enforcement}

为了确保数据保持安全，我们正在停用HTTP以支持HTTPS。Adobe Livefyre将于2018年月底完全停用所有HTTP和不安全SSL/TLS加密。这是旨在保护您和您的用户隐私的Adobe Standard。

## 谁受影响？ {#section_jf2_4yz_kcb}

这可能会影响拥有以下内容的Livefyre客户：

* 从CRM、CMS、WordPress或其他客户端调用服务器到服务器。
* 移动集成(Android和iOS应用程序)
* 自定义应用程序或自定义代码

## 我需要做什么？ {#section_unv_dc5_kcb}

1. 所有Livefyre客户必须通过HTTPS与所有通信通信，包括：

   * 服务器到服务器集成(CRM、CMS、WordPress等)
   * 移动集成(Android和iOS应用程序)
   * 自定义应用程序(Streamub SDK或直接编码)。

1. 服务器到服务器和Mobile HTTP客户端必须支持TLS1.2
1. 将主机名更改 `{*}.<network>.fyre.co``<network>.{*}.fyre.co`为。例如，主机名 `example.network.fyre.co` 更改为 `network.`example. fyre. co“例如：

   * `bootstrap.<network_name>.fyre.co` to to `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` to to `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` to to `<network_name>.admin.fyre.co`

## 如何知道我是否做了更改？ {#section_sqk_5d5_kcb}

您可能已经使用HTTPS，但Livefyre建议您仔细检查，尤其是如果您有：

* 来自CMS或CRM的服务器到服务器调用。
* 自定义代码或将SDK用于Javascript或Mobile中的自定义应用程序。
* 如果您的集成超过一年。
* 如果堆栈中的技术早于一年。

即使您已经使用HTTPS，您也必须验证API客户端是否支持TLS1.2。

## 如何验证我的API客户端是否支持TLS1.2？ {#section_nd1_j25_kcb}

负责开发站点的人员可以：

* 识别客户端软件。
* 识别版本。
* 阅读文档以确保API客户端支持TLS1.2。
* 根据需要开启调试模式。

## Java支持TLS1.2 {#section_lwn_rwk_ycb}

对于所有SSL连接，Oracle和更高版本的Oracle和OpenJDK JVM均配置为使用TLS1.2。如果您使用Java或更高版本，则无需执行任何其他操作。

Java或更早版本的用户应查阅有关如何启用TLS1.2的公共文档。

## 为什么需要更改主机名？ {#section_d5q_p25_kcb}

Livefyre在域上 `{*}.<network>.fyre.co` 没有SSL证书。只需更改HTTPS的URL即可中断应用程序。

## 我是否必须升级到Livefyre SDK的最新版本？ {#section_dw5_s25_kcb}

不会。您可以修补代码。要修补代码，您需要修改一些静态字符串并重新构建代码。如果您的HTTP客户端过时，您还需要升级或使用不同的升级。

## 这需要多长时间？ {#section_lgd_v25_kcb}

这一花费的时间取决于您的设置。如果您实施了简单的实施，则需要花费很少的时间来确认。如果您有许多自定义，则需要测试更新的代码并将其部署到服务器或应用程序商店中的新应用程序。为获得最佳效果，我们建议您初步审核作品，以便为任何长期工作做好准备。

## 完成此工作的时间轴是什么？ {#section_kgk_w25_kcb}

Livefyre将于2018年月底之前将端口80(HTTP)禁用到我们的服务，并且仅支持443(HTTPS)连接。尝试使用HTTP的浏览器和其他客户端将失败。

## 我何时需要完成此工作？ {#section_rvb_x25_kcb}

所有客户必须在2018年月底之前使用HTTPS。如果您无法达到此截止日期，请与我们的团队联系，网址为prioritysupport@livefyre.com。
