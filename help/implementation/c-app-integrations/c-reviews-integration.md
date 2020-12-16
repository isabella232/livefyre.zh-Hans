---
description: 允许客户对您的产品进行评级和评论。
seo-description: 允许客户对您的产品进行评级和评论。
seo-title: 评论
solution: Experience Manager
title: 评论
uuid: b740ee28-f6f9-4ae7-9fe7-61a5cde97bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 0%

---


# 评论{#reviews}

允许客户对您的产品进行评级和评论。

评论使社区成员能够为任何产品或服务提供星级评价和定性评论。

## 集成 {#section_kk5_15b_c1b}

要集成评论应用程序，请按照集成对话应用程序的过程进行操作。 请参阅[嵌入应用程序](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)。 以下是嵌入式审阅应用程序的示例。

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

正如“Building `CollectionMeta`”部分中所述，`CollectionMeta`是编码JSON对象。 在上例中，JSON对象在进行JWT编码前采用以下格式：

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## convConfig对象{#section_pzv_ytb_c1b}

如果您已经完成“入门”部分，您应该熟悉convConfig对象。 要启用“审阅”，请使用以下字段更新convConfig:

* **** ** alwaysShowEditoroptionalboolean:默认情况下，仅当用户按下“写入审阅”按钮后，才会显示审阅编辑器。将此参数设置为true可始终显示编辑器。

* **** ** apprequiredstring:用于审阅的应用程序名称。必须是“评论”。

* **** ** defaultSortoptionalstring:允许您为“审阅”选择默认的排序选项。可能的值有：最有用、评级最高、评级最低、最新和最旧。

* **** ** disableTitleoptionalboolean:在审阅编辑器中禁用和隐藏标题字段，该字段是必需字段，默认情况下是可见字段。默认值为true。

* **enableHalfRating** ** 选项布尔值：用于在默认星形选择模块上启用半分级。默认值为true。

* **hideShowReviewButton** ** 选项布尔值：控制是否 [!UICONTROL Show My Review] 显示按钮。设置为true可允许用户选择是显示还是显示自己的审阅。

* **** ** maxRatingoptionalinteger用于设置默认星形选择模块上显示的星形数。默认值为 5。最多可配置100个。

* **ratingSummaryEnabledoptional** ** 布尔值：用于在“审阅”应用程序上方显示评级摘要视图。必须启用此值才能使用ratingSummaryDelegate。 默认值为true。

## 查看集合元数据{#section_k1s_sqb_c1b}

* **type:** ** requiredstring:定义集合类型。必须为`reviews`。

* **** ** ratingDimensionalarray:此集合将使用的每种维类型的字符串数组。如果未指定，则仅允许1个维。

   例如，要允许用户对您的产品进行“设计”、“功能”和“性能”评级，请将阵列设置为：`ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **** ** ratingSubpartsopationalinteger:要在审阅的文本框中显示的分区数。子部件标签与参数一起传入，如下所示。

   >[!NOTE]
   >必须为每个子部件定义标签。

* **** ** ratingSubpartsIdsoptionalarray:允许您为评级集合中的每个子部件定义ID，该ID可用于在CSS和JavaScript中目标这些子部件元素。当用户发布评论时，每个`ratingSubpart`都将具有“`data-lf-subpart-id`”属性，并填充此ID。

>[!NOTE]
>
>要使用`ratingSubpartsIds`，还必须定义`ratingSubparts`参数，并且两个数组的长度必须匹配。

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
>如果您使用`ratingDimensions`，则必须使用`ratingSelectionDelegate`、`ratingDisplayDelegate`和`ratingSummaryDelegate`（如果要显示评级摘要）。

## 查看自定义{#section_khz_xmb_c1b}

### 配置星形图像

要更改全星的图像，类为`goog-ratings-star`。 将背景图像更改为您想要的任何图像。 默认情况下，星形为28 x 28像素。

### 使用半星配置星形图像

有半星，有两门课，每门一门。 半星的左侧为`fyre-rating-half-odd`，右侧为`fyre-rating-half-even`。 默认情况下，半星形为28 x 14像素。

### 配置星形工具提示值

要配置星形的工具提示值，请按照字符串自定义中所述的自定义文本操作。 设置后，请使用`ratingValues`键以及包含工具提示字符串的数组值。 如果禁用了半星形，则数组中的元素数应与`maxRating`（以上）相同。 如果启用半星形，则元素数应为2x `maxRating`。 数组中的第一个元素与最左边的星形（或半星形）元素对应，并从左到右继续。

### 切换“显示我的审阅”选项

要打开或关闭[!UICONTROL Show My Review]选项，请目标App配置中的`hideShowReviewButton`参数。

### 默认显示文本编辑器

仅在用户按[!UICONTROL write review]按钮后，才会显示审阅编辑器。 要默认显示此表单，请目标应用程序配置中的`alwaysShowEditor`参数。
