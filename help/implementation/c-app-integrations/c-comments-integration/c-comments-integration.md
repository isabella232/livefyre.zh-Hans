---
description: 在您的页面上启用实时注释。
seo-description: 在您的页面上启用实时注释。
seo-title: 注释
solution: Experience Manager
title: 注释
uuid: decad9b0-2074-4748-bd77-914008817bfa
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 2%

---


# 注释{#comments}

在您的页面上启用实时注释。 注释允许您将默认的注释系统替换为页面上的实时对话。

## 集成 {#concept_4093E8BAA96A464BA74D263DA031C0B0}

嵌入注释应用程序遵循嵌入核心应用程序的过程，该过程在“入门”>“嵌入应用程序”中介绍。

### 示例

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
        auth.delegate({ 
            login: function (callback) { 
                callback(null,{livefyre:'<userauthtoken>'}); 
            }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

如构建集合元部分中所述，集合元是编码的JSON对象。 在上例中，JSON对象在进行JWT编码前采用以下格式：

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

## NetworkConfig对象{#c-networkconfig-object}

`NetworkConfig`对象是JSON对象，用于为网络用户自定义身份验证系统。
`NetworkConfig`对象是包含以下参数的JSON对象：

| 参数 | 类型 | 描述 |
|---|---|---|
| **authDelegate** | **  requiredobject | 用于自定义网络用户的身份验证系统。 |
| **network** | 字符串&#x200B;*必填* | 由Livefyre提供的网络名称。 例如：*yourname.fyre.co.* |
| **attachmentDelegate** | *选* 项对象 | 用于指定在应用程序流中可见的媒体附件类型。 有关详细信息，请参阅[限制媒体](/help/implementation/c-app-customizations/c-restrict-media.md#c_restrict_media)。 |
| **字符串** | *选* 项对象 | 用于自定义任何Livefyre核心应用程序中HTML元素的文本字符串。 有关详细信息，请参阅[字符串自定义](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)。 |

## ConvConfig对象{#c-convconfig-object}

`convConfig`对象是JSON对象，用于指定Livefyre应用程序在页面上呈现的内容。

>[!NOTE]
>
>此处列出的`convConfig`对象参数不适用于“审阅”应用程序。 有关使用`convConfig`对象的“审阅”应用程序的集成信息，请参阅“审阅集成”。

`ConvConfig`对象包含以下必需参数：

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| **文章Id** | *必需* 字符串 | 唯一标识站点内的集合。 通常，这与CMS中的数据库主键或发布ID相对应。 例如：“42后”。 255 个字符限制.  注意： 如果使用文章URL作为文章ID，请确保字符串为MD5或SHA-1编码。 |
| **authPageReload** | *选*  项布尔值 | 适用于注释应用程序：允许您控制用户注释在身份验证过程中是否存储在本地。 如果为true，则用户输入评论，然后登录到应用程序，则该评论将存储在本地，并在登录和页面刷新后在内容字段中重新输入。 如果为false，则输入的内容将在登录过程中被清除，并且必须重新输入。 |
| **collectionMeta** | *必需* 字符串 | 有关集合的JWT编码的元数据。 有关详细信息，请参阅[CollectionMeta](#c_collectionmeta_object)对象。 |
| **el** | *必需* 字符串 | 内容流将呈现到的DOM元素的ID。 |
| **siteId** | *必需* 字符串 | 集合所属的网站或应用程序的Livefyre提供的ID。 例如：“303617”。 |

>[!NOTE]
>
>`app`参数对于“注释应用程序”实施不是必需的。

`ConvConfig`对象还可能包含以下可选参数：

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| **actionButtons** | *可选* 数组 | 要添加到“共享”和“标记”按钮旁边的内容的一组自定义操作按钮。 有关详细信息，请参阅添加自定义按钮。 |
| **动画** | *选* 项布尔值 | 定义动画是否将在Livefyre应用程序中运行。 设置为false可禁用动画。 默认值为true。 |
| **anonymousPargingEnabled** | *选* 项布尔值 | 定义客人用户是否具有标记内容的选项。 默认值为true。 |
| **browserType** | *可选* 字符串 | 定义应为其生成显示内容的设备。 这将导致CSS和某些功能发生更改以适合输入设备类型。 选项包括桌面、移动设备或平板电脑。 （如果留空，则默认为Google Agent确定显示格式。） |
| **校验和** | *推荐* 字符串 | 标识CollectionMeta的当前状态。 更改此值将导致Livefyre使用CollectionMeta中的新值更新服务器上的数据。 |
| **datetimeFormat** | *可选*  字符串对象函数 | 指定流式内容的日期时间格式。 有关详细信息，请参阅自定义日期和时间戳。 |
| **disableAvatars** | *选* 项布尔值 | 防止头像在应用程序流中呈现，从而减少加载到浏览器中的项目数。 默认为 false。 |
| **disableIE8Shim** | *选* 项布尔值 | 禁用Livefyre用于填充Internet Explorer 8的默认shiv，以支持HTML5元素。 Livefyre使用以下项目： [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv)。 默认为 false。注意： 如果此值为false，则必须使用某种类型的填充，才能调用Livefyre Chat以获得Internet Explorer 8支持。 |
| **disableThirdPartyAnalytics** | *选* 项布尔值 | 禁用Livefyre可用于内部测量的第三方分析系统(Quantserve和Google Analytics)。 默认为 false。 |
| **编辑器Css** | *选* 项对象 | 用于自定义注释编辑器样式。 您可以设置编辑器字段背景颜色以及编辑器中显示的文本的字体颜色、大小和系列的样式。  例如：`{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| **initialNumVisible** | *可选* 整数 | 允许您设置加载时在应用程序中显示的默认注释数。 这可以是1到50的整数。 |
| **initialNumVisibleLegacy** | *可选* 整数 | 允许您设置加载时在应用程序中可见的传统内容项目的默认数量。 这可以是1到50的整数。 如果未指定此参数，则默认为initialNumVisible。  例如：如果您的集合包含100个活动注释和100个传统注释，请设置initalNumVisible:10和initialNumVisibleLegacy:5，以显示10个活动注释（带有“显示更多”按钮）+ 5个存档注释（带有“显示更多”按钮）。 |
| **maxVisible** | *可选* 整数 | 设置聊天应用程序中最大可见的顶级内容片段数。 如果新内容流进入，则将从页面中删除该流底部的内容。 如果单击“显示更多……”按钮，则会忽略该参数，用户可自由显示所需的内容。 （使用此参数可控制高速流中页面上显示的项目数。） |
| **postToButtons** | *可选* 数组 | 用于配置嵌入实时博客应用程序时显示的提供者。 可用选项有两个(Twitter)、fb(Facebook)和li(LinkedIn)。 默认为[ tw, fb ]。 |
| **只读** | *选* 项布尔值 | 禁用集合的所有交互性。 如果为true，则用户将无法登录到流，并且无法发布、编辑、回复或类似内容。 如果为真，用户将能够标记和共享内容。 默认为 false。 |
| **流** | *选* 项对象 | 包含配置应用程序流的选项。 |
| **stream.catchup** | *可选* 整数 | 指定流应加载的当前时刻之前的秒数。 默认情况下，Livefyre加载50个内容，然后加载在这些内容和当前时间之间提交的所有内容。 在非常快速的使用情况下，内容发布速度可能过快，无法让应用程序“赶上”当前内容。 使用此设置可定义在加载初始内容后（在加载初始内容后），将发布内容的前一秒数。 |
| **stream.delay** | *可选* 整数 | 指定流请求之间的秒数。 使用此参数可帮助控制内容流并延迟更新DOM的频率。  注意： 如果设置得太大，流可能会落后。 |


>[!NOTE]
>
>在应用程序初始化过程中，您可以传递一个或多个`convConfig`对象，以在同一页面上显示多个应用程序。 请注意，额外的应用程序使用浏览器资源，并且性能可能会随着数量的增加而降低。

## CollectionMeta对象{#c-collectionmeta-object}

`CollectionMeta`对象是JSON对象，它指定要存储在集合中的元数据。

`CollectionMeta` 在传递到Livefyre之前，始终进行编码处理，以确保安全。编码值将传递到上图所示的`ConvConfig`对象。

>[!NOTE]
>
>必须添加服务器端代码才能对`CollectionMeta` JSON对象进行编码。 有关详细信息，请参阅构建服务器端令牌。

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| **文章Id** | *必需* 字符串 | 集合的唯一ID。 |
| **title** | *必需* 字符串 | 要应用于集合的标题。 这通常与显示应用程序的页面的标题相对应。  例如：“集成如此有趣！” <br>**注意：**  标题的最大字符长度为255个字符。标题字段不支持HTML实体。 请使用UTF-8对特殊字符进行编码。 |
| **url** | *必需* 字符串 | 要附加到此集合的规范绝对URL。 此URL将用于从Facebook和Twitter上共享的内容、电子邮件通知和Livefyre Studio中生成指向应用程序的链接。  <br>**注** 意Livefyre需要使用完全限定的域名；不需要端口号或回调来解析本地设置。如果在本地进行测试，请确保使用有效的基本URL域。 <br>例如： `https://customer.com` 有效，而 `https://localhost:5995` 非有效。一旦您将本地Web服务器设置为接受完全限定的域名，则不需要回呼或解决方案，并且本地开发可以按照预期进行。 |
| **type** | *必需* 字符串 | 集合类型。 必须为`livechat`。 |

`CollectionMeta`对象还可能包含以下可选参数：

| 参数 | 类型 | 描述 |
|---|---|---|
| **标记** | *可选* 字符串 | 单个关键字或短语的逗号分隔列表。 按Studio中的标记或使用搜索API搜索集合。 <br> **注意：** 虽然通过Studio添加的标记可能包含空格，但通过API输入的标记不能。使用下划线定义将在UI中显示空格的标记。 (例如：使用`Monday_Quarterback`在Studio中显示Monday Quarterback。) |

## 添加事件处理程序{#concept_06D8B811C98B4CC6B38C6340EBA176E5}

要注册事件处理函数，请在应用程序的回调函数中使用widget.on调用。

### 例如

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```
