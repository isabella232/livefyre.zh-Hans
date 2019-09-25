---
description: 实时博客允许您在报道实时活动时，从站点自己的编辑器中实时更新和图像。
seo-description: 实时博客允许您在报道实时活动时，从站点自己的编辑器中实时更新和图像。
seo-title: 实时博客
solution: Experience Manager
title: 实时博客
uuid: 5ca373f1-2008-45ab-9ec2-1e295af4e368
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# 实时博客{#live-blog}

实时博客允许您在报道实时活动时，从站点自己的编辑器中实时更新和图像。

## 实时博客 {#topic_574DEE2125A94B85BFB5C3D2C57C337E}

实时博客允许您在报道实时活动时，从站点自己的编辑器中实时更新和图像。

## 集成 {#c_live_blog_integration}

实时博客允许您在报道实时活动时，从站点自己的编辑器中实时更新和图像。

要嵌入实时博客应用程序，请按照嵌入应用程序的过程操作。 请参阅 [嵌入应用程序](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)。 以下是嵌入式实时博客应用程序的外观示例。

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
      network: "client-solutions.fyre.co" 
    }; 
    var convConfig = { 
      siteId: '347674', 
      articleId: '1', 
      el: 'livefyre', 
      collectionMeta: 'eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6IlRpdGxlIDEiLCJ1cmwiOiJodHRwOlwvXC9kZXYubGl2ZWZ5cmUuY29tIiwidGFncyI6InRhZzEsdGFnMiIsImNoZWNrc3VtIjoiY2Q0YTJjYWJkMTIxOTkyM2FjZGJhMjExOWY2NmYwNTUiLCJhcnRpY2xlSWQiOiIxIn0.Dq-ghi9KYmEPmagvCS1NPyYDRMGBujm735QaTRb7E7k', 
      checksum: '6e2e4faf7b95f896260fe695eafb34ba' 
    }; 
    
    Livefyre.require(['fyre.conv#3'], function(Conv) { 
        new Conv(networkConfig, [convConfig], function(blogWidget) {}); 
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

CollectionMeta是编码的JSON对象。 在上例中，JSON对象在进行JWT编码之前采用以下格式：

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "liveblog",  
"title": "Title 1" 
}
```

## NetworkConfig对象 {#c-networkconfig-object}

该对 `NetworkConfig` 象是一个JSON对象，用于为网络用户自定义身份验证系统。

该对 `NetworkConfig` 象是包含以下参数的JSON对象：

| 参数 | 类型 | 描述 |
|---|---|---|
| **authDelegate** | *必需对象* | 用于自定义网络用户的身份验证系统。 |
| **network** | *required* string A Livefyre提供的网络名称。 例如：您 *的姓名。fyre.co.* |
| **attachmentDelegate** | *可选对象* | 用于指定在应用程序流中可见的媒体附件的类型。 有关详细信息，请参 [阅限制媒体](../c-app-customizations/c-restrict-media.md#c_restrict_media)。 |
| **字符串** | *可选对象* | 用于自定义任何Livefyre核心应用程序中HTML元素的文本字符串。 有关详细信息，请参阅 [字符串自定义](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)。 |

## ConvConfig对象 {#c-convconfig-object}

该对 `convConfig` 象是一个JSON对象，用于指定Livefyre应用程序在页面上呈现的内容。

>[!NOTE]
>
>此处 `convConfig` 列出的对象参数不适用于“审阅”应用程序。 有关使用该对象的“审阅”应用程序的集成信 `convConfig` 息，请参阅“审阅集成”。

该对 `ConvConfig` 象包含以下必需参数：

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| **articleId** | *required* string | 唯一标识站点内的集合。 通常，这与CMS中的数据库主键或发布ID相对应。 例如：“42后”。 255 个字符限制.  注意： 如果使用文章URL作为articleId，请确保字符串为MD5或SHA-1编码。 |
| **collectionMeta** | *required* string | 关于集合的JWT编码的元数据。 有关详细信息，请参阅CollectionMeta对象。 |
| **el** | *required* string | 内容流将呈现到的DOM元素的ID。 |
| **siteId** | *required* string | 集合所属的网站或应用程序的Livefyre提供的ID。 例如：《303617》。 |

>[!NOTE]
>
>注 `app` 释应用程序实施不需要该参数。

该对 `ConvConfig` 象还可能包含以下可选参数：

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| **actionButtons** | *可选数组* | 要添加到“共享”和“标记”按钮旁边的内容的一组自定义操作按钮。 有关详细信息，请参阅添加自定义按钮。 |
| **动画** | *可选* boolean | 定义动画是否将在Livefyre应用程序内运行。 设置为false可禁用动画。 默认值为true。 |
| **anonymousPargingEnabled** | 布尔值 | 定义客人用户是否具有标记内容的选项。 默认值为true。 |
| browserType | *可选字符串* | 定义应为其生成显示内容的设备。 这将导致CSS和某些功能发生更改以适合输入设备类型。 选项包括桌面、移动设备或平板电脑。 （如果留空，将默认采用Google Agent确定显示格式。） |
| **校验和** | *可选字符串* （建议） | 标识CollectionMeta的当前状态。 更改此值将导致Livefyre使用CollectionMeta中的新值更新服务器上的数据。 |
| **datetimeFormat** | *可选字符串* 对象函数 | 指定流内容的日期时间格式。 有关详细信息，请参阅自定义日期和时间戳。 |
| disableAvatars | *可选* boolean | 防止在应用程序流中呈现头像，从而减少加载到浏览器中的项目数。 默认为 false。 |
| disableIE8Shim | *可选* boolean | 禁用Livefyre用于填充Internet Explorer 8的默认显示，以便支持HTML5元素。 Livefyre使用以下项目： [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) 。 默认为 false。注意： 如果此值为false，则必须使用某种类型的填充，才能调用Internet Explorer 8支持的Livefyre Chat。 |
| **disableThirdPartyAnalytics** | *可选* boolean | 禁用Livefyre可用于内部测量的第三方分析系统（Quantserve和Google Analytics）。 默认为 false。 |
| **editorCss** | *可选对象* | 用于自定义注释编辑器样式。 您可以设置编辑器字段背景颜色以及编辑器中显示的文本的字体颜色、大小和系列的样式。  例如：{背景：“#ccc”，颜色：“red”，字体：’30px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif’} |
| **initialNumVisible** | *可选整数* | 允许您设置加载时应用程序中可见的默认注释数。 这可以是1到50之间的整数。 |
| **initialNumVisibleLegacy** | *可选整数* | 允许您设置加载时在应用程序中可见的传统内容项目的默认数量。 这可以是1到50之间的整数。 如果未指定此参数，则默认为initialNumVisible。  例如：如果您的集合包含100个活动注释和100个传统注释，请将intialNumVisible:10和initialNumVisibleLegacy:5设置为显示10个活动注释（带有“显示更多”按钮）+ 5个存档注释（带有“显示更多”按钮）。 |
| **maxVisible** | *可选整数* | 设置聊天应用程序中最大可见的顶级内容片段数。 如果有新的内容流，则将从页面中删除该流底部的内容。 如果单击“显示更多……”按钮，则忽略该参数，用户可随意显示所需的内容。 （使用此参数可控制高速流中页面上显示的项目数。） |
| **postToButtons** | *可选数组* | 用于配置嵌入实时博客应用程序时显示的提供者。 可用选项有两个(Twitter)、fb(Facebook)和li(LinkedIn)。 默认为 [ tw, fb ]。 |
| **readOnly** | *可选* boolean | 禁用集合的所有交互性。 如果为true，则用户将无法登录流，也无法发布、编辑、回复或赞同内容。 如果为true，则用户将能够标记和共享内容。 默认为 false。 |
| **stream** | *可选对象* | 包含配置应用程序流的选项。 |
| stream.catchup | *可选整数* | 指定流应加载的当前时刻之前的秒数。 默认情况下，Livefyre加载50个内容，然后加载在这些内容和当前时间之间提交的所有内容。 在非常快的使用情况下，内容发布速度可能太快，使应用程序“赶上”当前内容。 使用此设置可定义在开始加载初始内容后将发布内容的前一秒数。 |
| **stream.delay** | *可选整数* | 指定流请求之间的秒数。 使用此参数可帮助控制内容流以及DOM的更新频率。  注意： 如果设置得过大，则流可能落后。 |


>[!NOTE]
>
>在应用程序初始化过程中，可 `convConfig` 以传递一个或多个对象，以在同一页面上显示多个应用程序。 请注意，额外的应用程序使用浏览器资源，并且性能可能会随着数量的增加而降低。

## CollectionMeta对象 {#c-collectionmeta-object}

该对 `CollectionMeta` 象是一个JSON对象，它指定要存储在集合中的元数据。

`CollectionMeta` 在传递到Livefyre之前始终进行编码，以确保安全。 编码值将传递到上面所 `ConvConfig` 示的对象。

>[!NOTE]
>
>必须添加服务器端代码才能对 `CollectionMeta` JSON对象进行编码。 有关详细信息，请参阅构建服务器端令牌。

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| **articleId** | *required* string | 集合的唯一ID。 |
| **title** | *required* string | 要应用于集合的标题。 这通常与显示应用程序的页面的标题相对应。  例如：“集成如此有趣！”注意： 标题的最大字符长度为255个字符。 标题字段不支持HTML实体。 请使用UTF-8对特殊字符进行编码。 |
| **url** | *required* string | 要附加到此集合的规范绝对URL。 此URL将用于从Facebook和Twitter上共享的内容、电子邮件通知和Livefyre studio中生成指向应用程序的链接。  注意： Livefyre需要使用完全限定的域名；不需要端口号或回调来解析本地设置。 如果在本地进行测试，请务必使用有效的基本URL域。 (例如： `https://customer.com` 有效，而 `https://localhost:5995` 非有效。)将本地Web服务器设置为接受完全限定的域名后，就不需要回调或分辨率，本地开发可以按预期进行。 |
| **type** | *required* String | 集合类型。 必须是livechat。 |

该对 `CollectionMeta` 象还可能包含以下可选参数：

| 参数 | 类型 | 描述 |
|---|---|---|
| **标记** | *可选字符串* | 单个关键字或短语的逗号分隔列表。 按Studio中的标记或使用搜索API搜索集合。 **** 注意：通过Studio添加的标记可能包含空格，但通过API输入的标记不能。 使用下划线定义将在UI中显示空格的标记。 (例如：使用Monday_Quarterback在Studio中显示Monday Quarterback。) |

## 添加事件处理函数 {#concept_D835C710A7214F6D921571E0770B6BC5}

要注册事件处理函数，请在应用程序的回调函数中使用widget.on调用。

例如：

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

