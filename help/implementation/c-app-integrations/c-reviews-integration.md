---
description: 允许客户对您的产品进行评级和检查。
seo-description: 允许客户对您的产品进行评级和检查。
seo-title: 评论
solution: Experience Manager
title: 评论
uuid: b740ee28-f6f9-4ae7-9fe7-61a5cde97bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# 评论 {#reviews}

允许客户对您的产品进行评级和检查。

评论允许社区成员对任何产品或服务提供星级评价和定性评论。

## 集成 {#section_kk5_15b_c1b}

要集成审阅应用程序，请按照集成对话应用程序的过程进行操作。 请参阅 [嵌入应用程序](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)。 以下是嵌入式审阅应用程序的示例。

### 示例

```
var networkConfig = { 
   network: "client-solutions-uat.fyre.co" 
}; 
  
var convConfig = { 
   siteId: '304059', 
   articleId: 'sh_col_22_1373478370_reviews', 
   el: 'livefyre-comments', 
   app: 'reviews', 
   ratingSummaryEnabled: true, 
   maxRating: 5, 
   collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5kaXJlY3R2LmNvbS9wZXJzb24vQW5uYS1QYXF1aW4tYjJGU0wwZHJLM051YldjOS1yZXZpZXdzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAiYXJ0aWNsZUlkIjogInNoX2NvbF8yMl8xMzczNDc4MzcwX3Jldmlld3MiLCAidHlwZSI6ICJyZXZpZXdzIiwgInRpdGxlIjogIlRCX1BhcXVpbl9yYXRpbmdzX3Jldmlld3MifQ.hes3KMwygCG-fFDQlkaB-XlxGjW6-iZ68xA4RRGqUl0' 
}; 
  
Livefyre.require(['fyre.conv#3'], function (Review) { 
   new Review(networkConfig, [convConfig], function (reviewWidget) {}); 
   auth.delegate({ 
      login: function (callback) { 
         callback(null,{livefyre:'<userauthtoken>'}); 
      }, 
   }); 
});
```

正如“构建”部分 `CollectionMeta` 所述， `CollectionMeta` 它是一个编码JSON对象。 在上例中，JSON对象在进行JWT编码之前采用以下格式：

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## convConfig对象 {#section_pzv_ytb_c1b}

如果您已经完成了“入门”部分，则应该熟悉convConfig对象。 要启用“审阅”，请使用以下字段更新convConfig:

* **alwaysShowEditor***可选* boolean:默认情况下，审阅编辑器仅在用户按下“写入审阅”按钮后显示。 将此参数设置为true可始终显示编辑器。

* **app** 必 *需字符* 串：用于审阅的应用程序名称。 必须是“评论”。

* **defaultSort** optional *字符串* :允许您为审阅选择默认的排序选项。 可能的值包括：最有帮助、评级最高、评级最低、最新和最旧。

* **disableTitle可** 选布尔 ** :在审阅编辑器中禁用和隐藏标题字段，该字段是必需的，默认情况下是可见的。 默认值为true。

* **enableHalfRating** *optional* boolean:用于在默认星形选择模块上启用半评级。 默认值为true。

* **hideShowReviewButton***可选* boolean:控制是否 [!UICONTROL Show My Review] 显示按钮。 设置为true可允许用户选择是显示还是显示自己的审阅。

* **maxRating** *optional* Integer用于设置默认星形选择模块中显示的星形数。 默认值为 5。最多可配置100个。

* **ratingSummaryEnabled***可选* boolean:用于在“审阅”应用程序上方显示评级摘要视图。 必须启用此选项才能使用ratingSummaryDelegate。 默认值为true。

## 查看集合元数据 {#section_k1s_sqb_c1b}

* **** type:必 *需的* 字符串：定义集合类型。 一定是 `reviews`的。

* **ratingDimensions***可选数组* :此集合将使用的每种类型维的字符串数组。 如果未指定，则仅允许1个维。

   例如，要允许用户对您的产品进行“设计”、“功能”和“性能”评级，请将阵列设置为： `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **ratingSubparts** 可 *选整数* :要在审阅的文本框中显示的分区数。 子部件标签随参数一起传递，如下图所示。

   >[!NOTE]
   >必须为每个子部件定义标签。

* **ratingSubpartsIds** 可 *选数* 组：允许您为评级集合中的每个子部件定义ID，该ID可用于在CSS和JavaScript中定位这些子部件元素。 当用户发布审阅时， `ratingSubpart` 每个用户都将具有 `data-lf-subpart-id`“”属性，并填充此ID。

>[!NOTE]
>
>要使用 `ratingSubpartsIds`，还必 `ratingSubparts` 须定义参数，并且两个数组的长度必须匹配。

```
networkConfig["strings"] = { 
   ratingSubpartPlaceholders: ['Pros...', 'Cons...'], 
   ratingSubpartTitles: ['Pros:', 'Cons:'], 
   ratingSubpartIds: ['pros', 'cons'], 
   reviewStreamTitle: 'Description:' 
} 
fyre.conv.load(networkConfig, [{ 
   app: 'reviews', 
   ratingSubparts: 2, 
    ... // More conv config settings 
}]);
```

>[!NOTE]
>
>如果您使用的 `ratingDimensions`是，则必须使用 `ratingSelectionDelegate`、 `ratingDisplayDelegate`和 `ratingSummaryDelegate` （如果要显示评级摘要）。

## 审阅自定义 {#section_khz_xmb_c1b}

### 配置星形图像

要更改满星的图像，类为 `goog-ratings-star`。 将背景图像更改为您想要的任何图像。 默认情况下，星形为28 x 28像素。

### 使用半星配置星形图像

有半颗星，有两门课，一门课分为两边。 半星形的左侧是， `fyre-rating-half-odd` 右侧是 `fyre-rating-half-even`。 默认情况下，半星形为28 x 14像素。

### 配置星形工具提示值

要配置星形的工具提示值，请按照字符串自定义中所述的自定义文本操作。 设置完该设置后，请使用键 `ratingValues` 和包含工具提示字符串的数组的值。 如果禁用了半星形，则数组中的元素数应与(上 `maxRating` 面)相同。 如果启用了半星形，则元素数应为2x `maxRating`。 数组中的第一个元素对应于最左侧的星形（或半星形）元素，并从左至右继续。

### 切换“显示我的审阅”选项

要打开或关 [!UICONTROL Show My Review] 闭选项，请在“应用程序”配 `hideShowReviewButton` 置中定位该参数。

### 默认情况下显示文本编辑器

仅在用户按下按钮后，才会显示审阅编 [!UICONTROL write review] 辑器。 要默认显示此表单，请在“应用程序”配 `alwaysShowEditor` 置中定位该参数。
