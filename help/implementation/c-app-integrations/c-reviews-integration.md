---
description: 允许客户评价和查看产品产品。
seo-description: 允许客户评价和查看产品产品。
seo-title: 评论
solution: Experience Manager
title: 评论
uuid: b740ee28-f6 f9-4ae7-9fe7-61a5 cde97 bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# 评论 {#reviews}

允许客户评价和查看产品产品。

审阅使社区成员能够为任何产品或服务贡献星级和定性审阅。

## 集成 {#section_kk5_15b_c1b}

要集成评论应用程序，请按照集成对话应用程序的过程操作。请参阅 [嵌入应用程序](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)。以下是嵌入式评论应用程序的示例。

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

如构建 `CollectionMeta` 部分中所述， `CollectionMeta` 是一个编码的JSON对象。在以上示例中，JSON对象在JWT编码之前采用以下格式：

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## CounConfig Object {#section_pzv_ytb_c1b}

如果您已经完成了“入门”部分，您应该熟悉ConferConfig对象。要启用评论，请使用以下字段更新ConverConfig：

* **alwaysShowEditor***可选* 布尔值：默认情况下，评论编辑器仅在用户按下“写审阅”按钮后才显示。将此参数设置为true可始终显示编辑器。

* **应用程序***所需* 的字符串：用于审阅的应用程序名称。必须为“评论”。

* **defaultSort***可选* 字符串：允许您选择审阅的默认排序选项。可能的值有：MosthelpFul、HighHead、LowePoints、最新和最旧。

* **标题标题***可选* 布尔值：禁用和隐藏评论编辑器中的标题字段，默认情况下该字段是必填字段。默认为true。

* **显示***可选* 的布尔值：用于在默认星形选择模块上启用半评级。默认为true。

* **hideshowreviewButton***可选* 布尔值：控制 [!UICONTROL Show My Review] 按钮是否显示。设置为true可允许用户选择是否显示或显示自己的审阅。

* **MaxRating***可选* 整数用于设置默认星形选择模块上显示的星星数量的整数。默认值为5。最多可配置100。

* **RatingSummaryEnabled***可选* 布尔值：用于在评论应用程序上方显示评级摘要视图。必须启用此操作才能使用RatingSummaryDelegate。默认为true。

## 审阅集合元数据 {#section_k1s_sqb_c1b}

* **类型：***必需* 字符串：定义集合类型。`reviews`必须如此。

* **RatingDimensions***可选* 数组：此Collection将使用的每种维度类型的字符串数组。如果未指定此项，则仅允许个维度。

   例如，要允许用户在“设计”、“功能”和“性能”上对产品进行评级，请将数组设置为： `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **RatingSubParts***可选* 整数：要在审阅的文本框中显示的分区数。子部件标签随参数一起传入，如下所示。

   >[!NOTE]
   >必须为每个子部件定义标签。

* **RatingSubParties***可选* 数组：允许您为评级集合中的每个子组定义一个ID，该ID可用于在CSS和JavaScript中定位这些子组件元素。当用户发布评论时，每个 `ratingSubpart` 用户都将在其上面添加“ `data-lf-subpart-id`”属性，该属性使用此ID填充。

>[!NOTE]
>
>要使用 `ratingSubpartsIds`， `ratingSubparts` 参数也必须定义，并且两个数组的长度必须匹配。

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
>如果您使用， `ratingDimensions`则必须使用 `ratingSelectionDelegate`、 `ratingDisplayDelegate`和 `ratingSummaryDelegate` (如果您要显示评级摘要)。

## 评论自定义 {#section_khz_xmb_c1b}

### 配置星形图像

要更改全星形的图像，该类为 `goog-ratings-star`。将背景图像更改为您需要的任何图像。默认情况下，星形为28x28像素。

### 用星形配置星形图像

对于半星，有两个类，分别为星形的每侧。下半星的左侧为， `fyre-rating-half-odd` 右侧 `fyre-rating-half-even`为。默认情况下，半星为28x14像素。

### 配置星星的工具提示值

要配置星形的工具提示值，请按照字符串自定义中描述的自定义文本进行操作。设置完毕后，请使用键 `ratingValues` 和值，该数组包含工具提示字符串。如果禁用了半星形，则数组中的元素的数量应与 `maxRating` (上面)相同。如果启用了半星，元素的数量应为2x `maxRating`。数组中的第一个元素对应于最左侧的星形(或半星)元素，并从左向右继续。

### 切换“显示我的评论”选项

要打开或关闭 [!UICONTROL Show My Review] 选项，请在应用程序配置中定位该 `hideShowReviewButton` 参数。

### 默认显示文本编辑器

只有在用户按下 [!UICONTROL write review] 按钮后，评论编辑器才会显示。要默认显示此表单，请在应用程序配置中定位该 `alwaysShowEditor` 参数。
