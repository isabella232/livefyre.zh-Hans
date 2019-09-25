---
description: 用于在您的站点上为Livefyre提供支持的核心Livefyre库。
seo-description: 用于在您的站点上为Livefyre提供支持的核心Livefyre库。
seo-title: Livefyre.js
solution: Experience Manager
title: Livefyre.js
uuid: 7b3eca57-d5e8-416d-badf-a9c51d10dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre.js {#livefyre-js}

用于在您的站点上为Livefyre提供支持的核心Livefyre库。

`Livefyre.js` 是可安装在每个支持Livefyre的网页上的核心库。 它定义了全局对 `window.Livefyre` 象和单个公共方法，可用于加载其他Livefyre javaScript库，这些库有助于嵌入Livefyre应用程序 `Livefyre.require`, [](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)[](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) 将身份验证提供者与Livefyre集成等。

## 添加到站点 {#section_cst_twg_xz}

将以下标 `<script>` 记添加到您的网页或网站模板。 如果可能，将其添加到HTML `<head>` 文档的部分，以便快速加载。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>此脚本将嵌入一个称为Livefyre.js侦察的很小（约1 Kb）的文件，该文件随后将通过访问网页的协议（HTTP或HTTPS）加载最新版Livefyre.js。

## Livefyre.require {#section_ipq_hwg_xz}

`Livefyre.require` 是自定义JavaScript模块加载器， [如curl.js](https://github.com/cujojs/curl) 或 [RequireJS](https://requirejs.org/)。 它可用于加载由Livefyre发布的大多数包，并呈现一条便捷、直观的集成路径。

可通过访问的包 `Livefyre.require` 使用语义版本 [控制版本](https://semver.org/)。 在特定版本或一系列版本上可能需要包，这样您的网页就可以自动受益于新的缺陷修复功能。 这样，您就可以在站点上集成Livefyre时获得灵活性。 您可以使用三个版本固定级别 `Livefyre.require`。

* **** package-name#1:固定到主版本v1。 您将获得所有可维护向后兼容API的新更新。 固定到主要版本以接收该版本的错误修复和次要功能增强。
* **** package-name#1.1:固定到次要版本v1.1。您将获得针对此次要版本的所有错误修复。 如果包的默认行为或功能范围发生更改，可能导致网页上出现新的意外行为，则Livefyre工程将始终颠覆该包的次要版本。 如果您希望收到自动错误修复，但不希望收到其他功能或对默认行为所做的更改，请将其固定到次要版本。
* **** package-name#1.1.1:固定到修补程序版本v1.1.1。即使存在错误修复，此嵌入的行为也不会更改。 如果您对站点的CSS自定义设置范围很广，且这些自定义设置取决于可能更改的包标记结构，或者如果您有其他理由希望您运行的Livefyre版本不会以任何方式更改，请将其固定到修补程序版本。

使用的示例集 `Livefyre.require` 成可能如下所示：

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

## 可用包 {#section_ygd_dwg_xz}

想知道哪个Livefyre javaScript包可通过 `Livefyre.require`? 您始终可以在以下网址找到受支持包及其最新版本的最新列表： [packages.html](https://cdn.livefyre.com/packages.html)。

## 测试预发行版包 {#section_pgm_dpg_xz}

有时，您可能希望测试即将推出的Livefyre包版本，以确保它在您的网站上正常工作或接受测试应您请求开发的功能。 除了包含语义版本范围之外，还可以指定预发行UAT环境。

例如，以下要求UAT版本、评论、 `fyre.conv`实时博客和聊天应用程序。

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
