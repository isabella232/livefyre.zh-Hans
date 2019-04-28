---
description: 在页面上启用实时注释。
seo-description: 在页面上启用实时注释。
seo-title: 注释
solution: Experience Manager
title: 注释
uuid: dececk9b0-2074-4748-bd77-914008817bfa
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 注释{#comments}

在页面上启用实时注释。注释允许您通过页面上的实时对话替换默认的注释系统。

## 集成 {#concept_4093E8BAA96A464BA74D263DA031C0B0}

嵌入评论应用程序遵循嵌入“入门”&gt;“嵌入应用程序”中描述的核心应用程序的过程。

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

如Building CollectionMeta部分中所述，CollectionMeta是一个编码的JSON对象。在以上示例中，JSON对象在JWT编码之前采用以下格式：

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

## NetworkConfig Object {#c-networkconfig-object}

`NetworkConfig` 该对象是为网络用户自定义身份验证系统的JSON对象。
`NetworkConfig` 该对象是一个JSON对象，其中包含以下参数：

| 参数 | Type | 描述 |
|---|---|---|
| **authDelegate** | *必需* 对象 | 用于自定义自定义网络用户的身份验证系统。 |
| **网络** | String *required* | Livefyre提供的网络名称。例如： *yourname. fyre. Co.* |
| **AttachmentDelegate** | *可选* 对象 | 用于指定在应用程序流中可见的媒体附件类型。有关详细信息，请参阅 [限制媒体](/help/implementation/c-app-customizations/c-restrict-media.md#c_restrict_media)。 |
| **strings** | *可选* 对象 | 用于自定义任何Livefyre核心应用程序中HTML元素的文本字符串。有关详细信息，请参阅 [字符串自定义](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)。 |

## CounConfig Object {#c-convconfig-object}

`convConfig` 该对象是一个JSON对象，用于指定Livefyre应用程序在页面上呈现的内容。

>[!NOTE]
>
>此处列出的 `convConfig` 对象参数不适用于评论应用程序。有关使用 `convConfig` 对象的审阅应用程序的集成信息，请参阅审阅集成。

`ConvConfig` 该对象包含以下必需参数：

| 参数 | Type | 描述 |
|--- |--- |--- |
| **articleID** | *必需* 字符串 | 在您的站点中唯一标识集合。通常，这与CMS中的数据库主要密钥或发布ID相对应。例如：“post-42”。255个字符限制。注意：如果将文章URL用作articleID，则确保字符串为MD或SHA-1编码。 |
| **AuthPageLoad** | *可选* 布尔值 | 应用于评论应用程序：允许您控制在身份验证过程中用户的注释是否存储在本地。如果为true，则用户输入评论后登录到应用程序，评论将存储在本地，并在登录和刷新后重新在内容字段中输入。如果为false，则输入的内容将在登录过程中擦除，并且必须重新键入。 |
| **CollectionMeta** | *必需* 字符串 | 有关集合的JWT编码元数据。有关更多信息，请参阅 [CollectionMeta](#c_collectionmeta_object) 对象。 |
| **el** | *必需* 字符串 | 将呈现内容流的DOM元素的ID。 |
| **SiteID** | *必需* 字符串 | 集合所属的网站或应用程序的Livefyre提供的ID。例如：“303617”。 |

>[!NOTE]
>
>评论应用程序实施不需要该 `app` 参数。

`ConvConfig` 该对象可能还包含以下可选参数：

| 参数 | Type | 描述 |
|--- |--- |--- |
| **ActionButtons** | *可选* 数组 | 要添加到“共享”和“标记”按钮旁边的一段内容的自定义操作按钮数组。有关更多信息，请参阅添加自定义按钮。 |
| **动画** | *可选* 布尔值 | 定义动画是否将在Livefyre应用程序中运行。设置为false以禁用动画。默认为true。 |
| **PhotosmousFlazingEnabled** | *可选* 布尔值 | 定义客人用户是否具有标记内容的选项。默认为true。 |
| **BrowserType** | *可选* 字符串 | 定义应生成显示内容的设备。这将导致CSS和一些功能更改以适应输入设备类型。选项包括台式机、移动设备或平板电脑。(如果留空，将默认为Google代理确定显示格式。) |
| **校验和** | *建议* 的字符串 | 标识CollectionMeta的当前状态。更改此值将导致Livefyre使用CollectionMeta中的新值更新服务器上的数据。 |
| **DateTimeFormat** | *可选* 字符串对象函数 | 指定流式内容的数据时间格式。有关更多信息，请参阅自定义日期和时间戳。 |
| **DisableAVats** | *可选* 布尔值 | 防止在应用程序流中渲染avatar，从而减少加载到浏览器中的项目数。默认为false。 |
| **disableIE8Shim** | *可选* 布尔值 | 禁用Livefyre用来填充Internet Explorer的默认shiv，以便支持HTML元素。Livefyre使用以下项目： [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) 。默认为false。注意：如果此值为false，则必须在调用Internet Explorer支持之前使用某些排序的多边形填充。 |
| **SocietthirdPartyAnalytics** | *可选* 布尔值 | 禁用Livefyre可用于内部测量的第三方分析系统(Quantservice和Google Analytics)。默认为false。 |
| **编辑CSS** | *可选* 对象 | 用于自定义注释编辑器样式。您可以设置编辑器字段背景颜色的样式，以及编辑器内显示的文本的字体颜色、大小和系列。例如： `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| **initialNumVisible** | *可选* 整数 | 允许您设置加载时在应用程序中可见的默认注释数。这可以是从到50的整数。 |
| **initialNumogbleLegacic** | *可选* 整数 | 允许您设置加载后应用程序中可见的旧版内容项目的默认数量。这可以是从到50的整数。如果未指定此参数，则默认为initialNumVisible。例如：如果您的Collection包含100个活动和100个旧注释，则设置initalNumVisible：和initialNumbubleLegacy：5，显示10个活动注释(带有“显示更多”按钮)+5归档注释(带有“显示更多”按钮)。 |
| **Maxible** | *可选* 整数 | 设置聊天应用程序中可见顶级内容的最大数量。如果有新的内容流，则流底部的内容将从页面中删除。如果单击“显示更多…”按钮，则忽略该参数，并且用户可随意显示所需的多个内容。(使用此参数可控制在高速流中页面上显示的项目数。) |
| **PosttoButton** | *可选* 数组 | 用于配置嵌入Live Blog应用程序时显示的提供者。可用的选项有tw(Twitter)、fb(Facebook)和li(LinkedIn)。默认为 [ tw fb ]。 |
| **只读** | *可选* 布尔值 | 禁用集合的所有交互性。如果为true，用户将无法登录流，并且无法发布、编辑、回复或类似内容。如果为true，用户将能够标记和共享内容。默认为false。 |
| **stream** | *可选* 对象 | 包含配置应用程序流的选项。 |
| **stream. catchup** | *可选* 整数 | 指定流应加载的当前秒数。默认情况下，Livefyre加载50份内容，然后加载在这些和当前时间之间提交的所有内容。在非常快速的用例中，内容可能会过快发布，以允许App“追赶”现有内容。使用此设置定义将发布内容的之前秒数(在初始内容加载之后)。 |
| **stream. delay** | *可选* 整数 | 指定流请求之间的秒数。使用此参数可帮助控制内容流并延迟DOM更新频率。注意：如果设置过大，则流可能会落后。 |


>[!NOTE]
>
>您可以在应用程序初始化过程中传递一个或多 `convConfig` 个对象，以在同一页面上显示多个应用程序。请注意，额外应用程序使用浏览器资源，且随着数量的增加，性能可能会降低。

## CollectionMeta对象 {#c-collectionmeta-object}

`CollectionMeta` 对象是一个JSON对象，它指定要存储在集合中的元数据。

`CollectionMeta` 始终编码，然后被传递到Livefyre以确保安全。编码的值将传递到上面显示的 `ConvConfig` 对象中。

>[!NOTE]
>
>必须添加服务器端代码才能对 `CollectionMeta` JSON对象进行编码。有关更多信息，请参阅构建服务器端令牌。

| 参数 | Type | 描述 |
|--- |--- |--- |
| **articleID** | *必需* 字符串 | 集合的唯一ID。 |
| **title** | *必需* 字符串 | 要应用于集合的标题。这通常与显示应用程序的页面的标题相对应。例如：“集成如此有趣！”<br>**注意：** 标题的最大字符长度为255个字符。标题字段不支持HTML实体。请使用UTF-8对特殊字符进行编码。 |
| **url** | *必需* 字符串 | 要附加到此集合的规范绝对URL。此URL用于从Facebook和Twitter、电子邮件通知和Livefyre Studio上共享的内容生成回应用程序的链接。<br>**注意** Livefyre需要使用完全限定的域名；不需要端口号或回调来解析本地设置。如果本地测试，请确定使用有效的基础URL域。<br>例如： `https://customer.com``https://localhost:5995` 有效，但不有效。将本地Web服务器设置为接受完全限定的域名后，无需回调或分辨率，本地开发可以按预期进行。 |
| **type** | *必需* 字符串 | 集合类型。`livechat`必须如此。 |

`CollectionMeta` 该对象可能还包含以下可选参数：

| 参数 | Type | 描述 |
|---|---|---|
| **标记** | *可选* 字符串 | 单个关键字或短语的以逗号分隔的列表。通过Studio中的标记或搜索API搜索集合。 <br> **注意：** 虽然通过Studio添加的标记可能包含空格，但是通过API输入的标记无法使用。使用下划线定义将在UI中显示空格的标记。(例如：用于 `Monday_Quarterback` 在Studio中显示星期一Quarterback。) |

## 添加事件句柄 {#concept_06D8B811C98B4CC6B38C6340EBA176E5}

要注册事件句柄，请在应用程序的回调函数内使用构件。

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
