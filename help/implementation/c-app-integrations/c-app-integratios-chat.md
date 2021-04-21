---
description: 向页面添加实时聊天。
title: 聊天
exl-id: f383bf19-0ff1-42ca-9b32-209a22679ad2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1429'
ht-degree: 3%

---

# 聊天{#chat}

向页面添加实时聊天。

通过聊天，受众可以参与围绕实时事件的实时对话。 内容以连续流的形式显示，鼓励快速参与展开的对话。

当前版本：聊天使用`fyre.conv v3.0.0.`

## 集成 {#concept_0A99792A7E89403F95D082D52D600F17}

嵌入聊天应用程序遵循嵌入核心应用程序的过程，该过程在入门> [嵌入应用程序](../c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md#using-livefyre-js-create-customize-apps)中介绍。

示例：

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
        new Conv(networkConfig, [convConfig], function(chatWidget) {}); 
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

如[CollectionMeta Token](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent)部分中所述，CollectionMeta是编码的JSON对象。 在上例中，JSON对象在JWT编码前采用以下格式：

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "livechat",  
"title": "Title 1" 
}
```

## NetworkConfig对象{#c-networkconfig-object}

`NetworkConfig`对象是为网络用户自定义身份验证系统的JSON对象。

`NetworkConfig`对象是包含以下参数的JSON对象：

| 参数 | 类型 | 描述 |
|---|---|---|
| authDelegate | ** requiredobject | 用于为自定义网络用户自定义身份验证系统。 |
| network | *必* 需字符串 | Livefyre提供的网络名称。 例如：*yourname.fyre.co.* |
| attachmentDelegate | 对象 | 用于指定在应用程序流中可见的媒体附件的类型。 有关详细信息，请参阅[限制媒体](../c-app-customizations/c-restrict-media.md#c_restrict_media)。 |
| 字符串 | *选* 项对象 | 用于自定义任何Livefyre核心应用程序中HTML元素的文本字符串。 有关详细信息，请参阅[字符串自定义](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)。 |

## ConvConfig对象{#c-convconfig-object}

`convConfig`对象是JSON对象，用于指定Livefyre应用程序在页面上呈现的内容。

>[!NOTE]
>
>此处列出的`convConfig`对象参数不适用于“审阅”应用程序。 有关使用`convConfig`对象的“审阅”应用程序的集成信息，请参阅“审阅集成”。

`ConvConfig`对象包含以下必需参数：

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| articleId | *必* 需字符串 | 在您的网站中唯一标识集合。 通常，这对应于CMS中的数据库主键或帖子ID。 例如：“42后”。 255 个字符限制.  注意： 如果使用文章URL作为articleId，请确保字符串是MD5或SHA-1编码的。 |
| collectionMeta | *必* 需字符串 | 有关集合的JWT编码的元数据。 有关详细信息，请参阅[CollectionMeta Object](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent)。 |
| el | *必* 需字符串 | 内容流将呈现到的DOM元素的ID。 |
| siteId | *必* 需字符串 | Livefyre为集合所属的网站或应用程序提供的ID。 例如：“303617”。 |

>[!NOTE]
>
>`app`参数不是Comments App实现所必需的。

`ConvConfig`对象还可能包含以下可选参数：

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| actionButton | *可选* 数组 | 要添加到“共享”和“标志”按钮旁边的内容的自定义操作按钮数组。 有关详细信息，请参阅添加自定义按钮。 |
| 动画 | *选* 项布尔值 | 定义动画是否将在Livefyre应用程序内运行。 设置为false可禁用动画。 默认为true。 |
| anonymousLaggingEnabled | *选* 项布尔值 | 定义客人用户是否具有标记内容的选项。 默认值为true。 |
| browserType | *可选* 字符串 | 定义应为其生成显示内容的设备。 这将导致CSS和某些功能发生更改以适合输入设备类型。 选项包括台式机、手机或平板电脑。 （如果留空，将默认采用Google Agent确定显示格式。） |
| 校验和 | *推* 荐的字符串（推荐） | 标识CollectionMeta的当前状态。 更改此值将导致Livefyre使用CollectionMeta中的新值更新服务器上的数据。 |
| datetimeFormat | *选* 项字符串对象函数 | 指定流内容的日期时间格式。 有关详细信息，请参阅自定义日期和时间戳。 |
| disableAvatars | *选* 项布尔值 | 防止头像在应用程序流中呈现，从而减少加载到浏览器中的项目数。 默认为 false。 |
| disableIE8Shim | *选* 项布尔值 | 禁用Livefyre用来对Internet Explorer 8进行填充的默认shiv，以便支持HTML5元素。 Livefyre使用以下项目： [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv)。 默认为 false。注意： 如果此值为false，则在调用Internet Explorer 8支持的Livefyre聊天之前，必须使用某种类型的填充。 |
| disableThirdPartyAnalytics | ** optionalbBoolean | 禁用Livefyre可用于内部测量的第三方分析系统(Quantserve和Google Analytics)。 默认为 false。 |
| editorCss | *选* 项对象 | 用于自定义注释编辑器样式。 您可以设置编辑器字段背景颜色以及编辑器中显示的文本的字体颜色、大小和系列的样式。  例如：`{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| initialNumVisible | *可选* 整数 | 允许您设置加载时在应用程序中显示的默认注释数。 这可以是1到50之间的整数。 |
| initialNumVisibleLegacy | *可选* 整数 | 允许您设置加载时在应用程序中显示的默认旧版内容项目数。 这可以是1到50之间的整数。 如果未指定此参数，则默认为initialNumVisible。  例如：如果您的集合包含100个活动注释和100个旧版注释，请设置initalNumVisible:10和initialNumVisibleLegacy:5，以显示10个活动注释（使用“显示更多”按钮）+ 5个存档注释（使用“显示更多”按钮）。 |
| maxVisible | *可选* 整数 | 设置聊天应用程序中最大可见顶级内容片段数。 如果有新的内容流进入，则将从页面中删除该流底部的内容。 如果单击“显示更多……”按钮，则会忽略该参数，用户可以随意显示所需的内容。 （使用此参数可控制高速流中页面上显示的项目数。） |
| postToButtons | *可选* 数组 | 用于配置嵌入实时博客应用程序时显示的提供者。 可用选项有tw(Twitter)、fb(Facebook)和li(LinkedIn)。 默认为[ tw， fb ]。 |
| readOnly | *选* 项布尔值 | 禁用集合的所有交互性。 如果为true，则用户将无法登录流，并且无法发布、编辑、回复或称赞内容。 如果为true，则用户将能够标记和共享内容。 默认为 false。 |
| 流 | *选* 项对象 | 包含配置应用程序流的选项。 |
| stream.catchup | *可选* 整数 | 指定流应加载的当前时刻之前的秒数。 默认情况下，Livefyre加载50个内容，然后加载在这些内容和当前时间之间提交的所有内容。 在非常快速的使用情况下，内容发布可能太快，无法让应用程序“赶上”当前状态。 使用此设置可定义当前要发布内容的秒数（在初始内容加载后）。 |
| stream.delay | *可选* 整数 | 指定流请求之间的秒数。 使用此参数可帮助控制内容流和延迟更新DOM的频率。  注意： 如果设置得太大，流可能会落在后面。 |


>[!NOTE]
>
>您可以在应用程序初始化期间传递一个或多个`convConfig`对象，以在同一页面上显示多个应用程序。 请注意，额外的应用程序使用浏览器资源，并且性能可能会随着数量的增加而降低。

## CollectionMeta对象{#c-collectionmeta-object}

`CollectionMeta`对象是一个JSON对象，它指定要存储在集合中的元数据。

`CollectionMeta` 在传递到Livefyre之前始终进行编码，以确保安全性。编码值将传递到上面显示的`ConvConfig`对象。

>[!NOTE]
>
>必须添加服务器端代码才能对`CollectionMeta` JSON对象进行编码。 有关详细信息，请参阅构建服务器端令牌。

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| articleId | *必* 需字符串 | 集合的唯一ID。 |
| title | *必* 需字符串 | 要应用于收藏集的标题。 这通常与显示应用程序的页面的标题相对应。  例如：“集成如此有趣！”  注意： 标题的最大字符长度为255个字符。 标题字段不支持HTML实体。 请使用UTF-8对特殊字符进行编码。 |
| url | *必* 需字符串 | 要附加到此集合的规范绝对URL。 此URL将用于从Facebook和Twitter上共享的内容、电子邮件通知和Livefyre Studio中生成指向应用程序的链接。  注意： Livefyre需要使用完全限定的域名；不需要端口号或回调来解析本地设置。 如果在本地进行测试，请务必使用有效的基本URL域。 (例如：`https://customer.com`有效，而`https://localhost:5995`无效。) 设置本地Web服务器以接受完全限定的域名后，就不需要回调或解决方案，本地开发可以按预期进行。 |
| type | *必* 需字符串 | 集合类型。 必须为livechat。 |

`CollectionMeta`对象还可能包含以下可选参数：

| 参数 | 类型 | 描述 |
|--- |--- |--- |
| 标记 | *可选* 字符串 | 单个关键字或短语的逗号分隔列表。 在Studio中或使用搜索API按标记搜索集合。  注意：虽然通过Studio添加的标记可能包含空格，但通过API输入的标记不能。 使用下划线定义将在UI中显示空格的标记。 (例如：使用Monady_Quarterback在Studio中显示Monday Quarterback。) |

## 添加事件处理程序{#concept_E7C17EFB43F24F1A8572E60C69176C6D}

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

有关详细信息以及可用事件的列表，请参阅[Javascript事件](../c-app-customizations/c-javascript-events.md#c_javascript_events)。
