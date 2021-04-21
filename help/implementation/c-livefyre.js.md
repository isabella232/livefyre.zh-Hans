---
description: 用于在您的站点上为Livefyre提供支持的核心Livefyre库。
title: Livefyre.js
exl-id: 82083dc0-3b4a-467c-bad7-dbf242ab5bbd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Livefyre.js {#livefyre-js}

用于在您的站点上为Livefyre提供支持的核心Livefyre库。

`Livefyre.js` 是您可以在每个支持Livefyre的网页上安装的核心库。它定义全局`window.Livefyre`对象和单个公共方法`Livefyre.require`，可用于加载其他Livefyre JavaScript库，帮助[嵌入Livefyre应用程序](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)、[将身份验证提供商与Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)集成等。

## 添加到您的站点{#section_cst_twg_xz}

将以下`<script>`标记添加到您的网页或网站模板。 如果可能，将其添加到HTML文档的`<head>`部分，以便快速加载。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>此脚本将嵌入一个很小(~1 Kb)的文件，称为Livefyre.js侦察，该文件随后将通过访问您的网页的协议（HTTP或HTTPS）加载最新版Livefyre.js。

## Livefyre.require {#section_ipq_hwg_xz}

`Livefyre.require` 是自定义JavaScript模块加载 [器，如](https://github.com/cujojs/curl) curl. [jsor RequireJS](https://requirejs.org/)。它可用于加载由Livefyre发布的大多数包，并提供一条便捷、直观的集成路径。

可通过`Livefyre.require`访问的包使用[语义版本控制](https://semver.org/)进行版本控制。 在特定版本或一系列版本上可能需要包，因此您的网页可以自动从新的错误修复功能中受益。 这样，您就可以在站点上集成Livefyre时获得灵活性。 您可以与`Livefyre.require`一起使用三种版本固定级别。

* **package-name#1：固定** 到主版本v1。您将获得所有可维护向后兼容API的新更新。 固定到主版本以接收该版本的错误修复和次要功能增强。
* **package-name#1.1：固定** 到次要版本v1.1。对于此次要版本，您会收到所有错误修复。如果包的默认行为或功能范围发生更改，可能导致网页上出现意外的新行为，Livefyre工程将始终使软件包的次要版本受到冲击。 如果您希望接收自动错误修复，但没有其他功能或更改默认行为，请固定到次要版本。
* **package-name#1.1.1：固定** 到修补程序版本v1.1.1。即使存在错误修复，此嵌入的行为也不会改变。如果您的站点具有大量CSS自定义项，这些自定义项取决于可能更改的包标记结构，或者您有其他理由希望您运行的Livefyre版本不会以任何方式更改，请将其固定到修补程序版本。

使用`Livefyre.require`的示例集成可能如下所示：

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

## 可用包{#section_ygd_dwg_xz}

想知道通过`Livefyre.require`可以使用哪些Livefyre JavaScript包？ 您始终可以在以下网址找到受支持程序包及其最新版本的最新列表:[packages.html](https://cdn.livefyre.com/packages.html)。

## 测试软件包的预发行版{#section_pgm_dpg_xz}

有时，您可能希望测试即将推出的Livefyre包版本，以确保它在您的网站上正常工作或接受测试应您请求开发的功能。 除了包括语义版本范围外，还可以指定预发行UAT环境。

例如，以下版本需要`fyre.conv`的UAT版本、评论、实时博客和聊天应用程序。

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
