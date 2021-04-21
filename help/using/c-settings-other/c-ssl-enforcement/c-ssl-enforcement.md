---
title: SSL强制
description: SSL强制
exl-id: 033e15d9-84f6-42d5-8457-04263dcbd11c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 2%

---

# SSL强制{#ssl-enforcement}

为确保您的数据保持安全，我们弃用了HTTPS。 Adobe Livefyre将在2018年8月底之前完全禁用所有HTTP和不安全的SSL/TLS密码。 这是一款Adobe标准，旨在保护您和您用户的隐私。

## 谁受影响？{#section_jf2_4yz_kcb}

这可能会影响具有以下功能的Livefyre客户：

* 从其CRM、CMS、WordPress或其他客户端进行服务器到服务器的调用。
* 移动集成（Android和iOS应用程序）
* 自定义应用程序或自定义代码

## 我需要做些什么？{#section_unv_dc5_kcb}

1. 所有Livefyre客户必须通过HTTPS与所有API通信，以便处理所有流量，包括：

   * 服务器到服务器集成（CRM、CMS、WordPress等）
   * 移动集成（Android和iOS应用程序）
   * 自定义应用程序（Streamhub SDK或直接编码）。

1. 服务器到服务器和移动HTTP客户端必须支持TLS 1.2
1. 将主机名从`{*}.<network>.fyre.co`更改为`<network>.{*}.fyre.co`。 例如，主机名`example.network.fyre.co`更改为`network.`example.fyre.co&quot;。 例如：

   * `bootstrap.<network_name>.fyre.co` 更改为 `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` 更改为 `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` 更改为 `<network_name>.admin.fyre.co`

## 我如何知道我是否做了更改？{#section_sqk_5d5_kcb}

您可能已使用HTTPS，但Livefyre建议您进行多次检查，尤其是：

* 从CMS或CRM进行服务器到服务器的调用。
* 自定义代码或在Javascript或移动设备中对自定义应用程序使用SDK。
* 如果您的集成已过一年。
* 如果堆栈中的技术比一年旧。

即使您已经使用HTTPS，也必须验证您的API客户端是否支持TLS 1.2。

## 如何验证我的API客户端是否支持TLS 1.2?{#section_nd1_j25_kcb}

负责网站开发的人员可以：

* 识别客户端软件。
* 识别版本。
* 阅读文档以确保API客户端支持TLS 1.2。
* 根据需要打开调试模式。

## 对TLS 1.2 {#section_lwn_rwk_ycb}的Java支持

Oracle和OpenJDK JVM（适用于Java 8和更高版本）配置为默认使用TLS 1.2来连接所有SSL连接。 如果您使用Java 8或更高版本，则无需执行任何其他操作。

Java 7或更早版本的用户应查阅有关如何启用TLS 1.2的公开文档。

## 我为何需要更改主机名？{#section_d5q_p25_kcb}

Livefyre在`{*}.<network>.fyre.co`域上没有SSL证书。 只需将URL更改为HTTPS，应用程序就会中断。

## 我是否必须升级到最新版Livefyre SDK?{#section_dw5_s25_kcb}

不会。您可以改为修补代码。 要修补代码，请修改一些静态字符串并重新构建代码。 如果您的HTTP客户端已过时，您还需要升级该客户端或使用其他客户端。

## 这需要多久？{#section_lgd_v25_kcb}

这所花费的时间长短取决于您的设置。 如果实施简单，则确认无需太多时间。 如果您有许多自定义项，您需要测试更新的代码并将其部署到服务器或新应用程序到应用程序商店。 为获得最佳效果，我们建议您对工作进行初步审核，以便您能够计划任何较长期的工作。

## 完成此工作的时间表是什么？{#section_kgk_w25_kcb}

Livefyre将在2018年8月底之前禁用服务的端口80(HTTP)，并仅支持与443(HTTPS)的连接。 尝试使用HTTP的浏览器和其他客户端将失败。

## 我什么时候需要完成这项工作？{#section_rvb_x25_kcb}

所有客户必须在2018年7月底之前使用HTTPS。 如果您无法达到此截止日期，请通过prioritysupport@livefyre.com与我们的团队联系。
