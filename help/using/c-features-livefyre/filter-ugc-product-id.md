---
description: 按产品ID筛选UGC允许您在多个页面上嵌入相同的应用程序，同时为每个页面显示不同的产品特定UGC。
seo-description: 按产品ID筛选UGC允许您在多个页面上嵌入相同的应用程序，同时为每个页面显示不同的产品特定UGC。
seo-title: 按产品ID过滤UGC
title: 按产品ID过滤UGC
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 按产品ID过滤UGC {#filter-ugc-product-id}

按产品ID筛选UGC允许您在多个页面上嵌入相同的应用程序，同时为每个页面显示不同的产品特定UGC。

要按产品ID筛选UGC，请按照以下步骤操作：

1. 在Livefyre Studio中，导航 **[!UICONTROL Apps]** 到选项卡。

1. 选择要修改的应用程序。

1. 选择左边栏中的设计人员选项卡。

1. 启用 **[!UICONTROL Filter UGC by Product ID]**。

![](assets/filter-ugc-product-id.png)

1. 选择包含您要筛选UGC的产品或产品的顶级产品文件夹。
使用CTRL/Command+单击可选择多个文件夹。

1. 禁用 **[!UICONTROL Show related content]**。
启用此功能后，使用 `data-lf-attr-product` 属性筛选的内容将先显示，后跟应用程序中的所有其他内容。

1. 单击 **[!UICONTROL Publish]**。

1. 插入要筛选的产品ID，然后进入生成的代码。

>[!NOTE]
>
>要定位产品ID，请导航 **[!UICONTROL Settings > Products]**到。找到所需的产品并选择该产品，此时将显示ID。

例如，为媒体墙应用程序生成以下代码：

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published" datalf-
env="prod" data-lf-read-only="" data-lf-attr-product="<product
 1>,<product 2>"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

要标记某个产品，请用 `<product 1>` 所需的产品ID替换 `data-lf-attr-product` 该属性。您可以通过添加其他以逗号分隔的产品ID标记一个或多个产品。产品必须包含在在步骤中选择的顶级产品一个或多个文件夹中。

修改后的代码段将显示为：

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published"
 data-lf-env="prod" data-lf-read-only="" data-lf-attrproduct="
109,47"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

应用程序现在只显示标记的产品ID。