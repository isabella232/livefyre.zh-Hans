---
description: 用于为站点上Livefyre供电的核心Livefyre库。
seo-description: 用于为站点上Livefyre供电的核心Livefyre库。
seo-title: Livefyre. js
solution: Experience Manager
title: Livefyre. js
uuid: 7b3a57-d5 e8-416d-badf-a9 c51 d10 dd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre. js {#livefyre-js}

用于为站点上Livefyre供电的核心Livefyre库。

`Livefyre.js` 是可在每个启用Livefyre的网页上安装的核心库。它定义了全局 `window.Livefyre` 对象和一种公共方法， `Livefyre.require`它可用于加载其他有助于 [嵌入Livefyre应用程序的Livefyre JavaScript库](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)，将 [您的身份验证提供程序与Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) 集成，等等。

## 添加到站点 {#section_cst_twg_xz}

将以下 `<script>` 标记添加到网页或网站模板。如有可能，请将其添加到HTML文档的 `<head>` 部分，以便快速加载。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>此脚本将嵌入一个名为Livefyre. js的非常小的(~1Kb)文件，它随后将加载Livefyre. js的最新版本，该文件在与您的网页(HTTP或HTTPS)被访问的协议上加载。

## Livefyre.要求 {#section_ipq_hwg_xz}

`Livefyre.require` 是一个自定义JavaScript模块加载器，如 [currl. js](https://github.com/cujojs/curl) 或 [RequireJS](https://requirejs.org/)。它可用于加载Livefyre发布的大多数包，并提供方便直观的集成路径。

可访问的包使用 `Livefyre.require`[语义版本控制](https://semver.org/)进行版本控制。软件包可在特定版本或各版本的版本中要求使用，因此您的网页可以自动受益于新缺陷修复功能。这使您能够在站点上集成Livefyre时灵活。有三个级别的版本固定可用于 `Livefyre.require`。

* **package-name#1：** 固定到主要版本v1。您将获得所有保持向后兼容API的新更新。固定到主要版本以获得该版本的错误修复和次要功能增强。
* **package-name#1.1：** 固定到v1.1次要版本。您将获得此次要版本的所有错误修复。如果Livefyre的默认行为或功能范围更改方式可能会导致网页上出现新的意外行为，则Livefyre Engineering将始终干扰包的次要版本。如果您希望接收自动缺陷修复，但没有其他功能或更改默认行为，则固定到次要版本。
* **package-name#1.1.1：** 固定到修补版本v1.1.1。即使存在缺陷，此嵌入的行为也决不会更改。如果您为站点提供了基于包的标记结构的广泛CSS自定义，则固定到修补版本，或者如果您有其他原因，即您正在运行的Livefyre版本不会以任何方式发生更改。

使用的示例集成 `Livefyre.require` 可能如下：

```
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
  
<!-- Then load up all the desired Livefyre packages and Do Stuff in the callback --> 
<script> 
Livefyre.require([ 
    'lfawesome#1', 
    'lfsuperawesome#2.1.2' 
], function (LFAwesome, LFSuperAwesome) { 
    var greatness = new LFAwesome(); 
    // etc.. 
}); 
</script>
```

## 可用的包 {#section_ygd_dwg_xz}

想知道哪些Livefyre JavaScript包可用 `Livefyre.require`？您始终可以在此处找到支持的包及其最新版本的最新列表： [packages.html](https://cdn.livefyre.com/packages.html)。

## 测试预发行版本的软件包 {#section_pgm_dpg_xz}

有时，您可能想要测试一个即将发布的Livefyre包版本，以确保它能够在您的网站上运行，或对根据您请求开发的某个功能进行测试。除了包含语义版本范围外，还可以指定预发布UAT环境。

例如，以下内容需要UAT版本 `fyre.conv`、评论、Live Blog和聊天应用程序。

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
