---
description: null
seo-description: null
seo-title: 向页面添加引用
solution: Experience Manager
title: 向页面添加引用
uuid: 6499c45a-3773-4adb-a6 c7-22a628309 afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# 向页面添加引用 {#adding-sidenotes-to-a-page}

Livefyre提供了多个配置选项，用于在页面上放置SideNote：

* 选择器选项定义应显示Siten说明的元素。
* 锚点代表可显示的元素。
* 自定义线程容器允许您定义Sidenes线程将与显示的内容相关的位置。
* 使用“席位数”选项可显示在给定位置添加的席位数。
* 使用多 `ConvConfig` 个对象在单个页面上将Siden表示添加到多篇文章。

## 选择器 {#section_wyj_4sv_sy}

选择器选项允许SiteNote在页面上查找内容。此选项的值允许您动态确定将使用的元素。它可以是选择器字符串(如“# content p、# content img”)、一个jQuery对象(如 `$(‘#content’)`)、DOM元素数组或具有两个属性的对象：包括和排除。Siten表示应用程序随后将在页面上使用指定元素或匹配元素。如果使用了包括和排除属性，则SiteNote首先将解析页面以查找包含属性上的所有元素，然后删除在exclude属性上找到的任何元素。

## 锚点 {#section_ehq_psv_sy}

锚点代表一个元素，其内容可以为siteded。锚点元素可包含文本或图像。在应用程序构建过程中传递的选择器选项将决定锚点元素。

## 锚点ID {#section_rsb_rsv_sy}

页面上的锚点使用 `data-lf-anchor-id`a.

要自行设置锚点的ID，请向要映射到锚点的元素添加属性 `data-lf-custom-anchor-id` 。当锚点自动检测失败时，此功能非常有用。

例如，如果您计划对图像的桌面和移动版本使用不同的URL，则可能会将两个不同的URL映射到不同的锚点。如果相反，您的HTML在 `data-lf-custom-anchor-id` 移动和桌面设备上提供相同的内容，那么图像元素将视为单一锚点。

锚点的类型是动态确定的，但也可以使用 `data-lf-custom-anchor-type` 属性显式设置。

>[!NOTE]
>
>必须使用枚举编号值。

可用类型有：

* **文本：** 1
* **图像：** 2
* **媒体：** 3
* **丰富：** 个

有关 [如何使用](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md)`updateAnchors` 方法向页面动态添加SitenOte内容的更多信息，请参阅updateAnchors方法。

## 自定义线程容器 {#section_jdh_btv_sy}

使用该 `threadContainerEl` 选项指定SiteNote线程的位置，而非默认位置。默认情况下，当锚点被激活时，Sideon表示将显示在相关内容的旁边或下方。要更改此默认值，请使用应 `threadContainerEl` 显示线程的元素。

此选项的值与选择器选项的作用相同，只是将仅使用第一个有效元素。

## Siten表示计数 {#section_pld_ntv_sy}

使用 `numSidenotesEl` 选项在页面上嵌入可选的Sidones计数构件。此选项接受与选择器选项相同的输入，但只使用输入数组中的第一个有效元素。

构件将装饰提供的或匹配的元素，并将包括Siden表示输入图标、在此位置输入的席位数和帮助图标。

单击该构件将显示一个弹出窗口，其中包含SiteNote简短说明以及如何使用它们。

解释和示例文本都可使用自定义字符串( `questionExplanation` 以及 `questionMockText`分别)进行配置。计数构件的外观和弹出窗口也可以使用自定义样式( `numSidenotes` 并且 `numSidenotesPopover`分别使用)进行配置。

## 向单个页面添加多个集合 {#section_pjl_ptv_sy}

Livefyre允许您将多个集合添加到单个页面。例如，如果页面包含三个新闻故事，您可能希望包含三个单独的Sidenes应用程序迭代。为此，必须为要构建的SiteNote实例定义单独 `ConvConfig` 的对象。例如：

```
<html> 
   <head> 
      <script src="//cdn.livefyre.com/Livefyre.js"></script> 
   </head> 
<body> 
   <h2>Story #1</h2> 
   <div id="story1"> 
      <p class="sidenotes">stuff #1</p> 
      <p class="sidenotes">more stuff #1</p> 
   </div> 
   <hr /> 
   <h2>Story #2</h2> 
   <div id="story2"> 
      <p class="sidenotes">stuff #2</p> 
      <p class="sidenotes">more stuff #2</p> 
      <p class="sidenotes">more and more stuff</p> 
   </div> 
   <hr /> 
   <script type="text/javascript"> 
      var convConfig_story1 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Article ID>', 
         selectors: '#story1 > p.sidenotes', 
         collectionMeta: '<First collectionMeta>' 
      }; 
  
      var convConfig_story2 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Second Article ID>', 
         selectors: '#story2 > p.sidenotes', 
         collectionMeta: '<Second collectionMeta>' 
      }; 
  
      Livefyre.require(['sidenotes#1', 'auth'], function(Sidenotes, auth) { 
         new Sidenotes(convConfig_story1); 
         new Sidenotes(convConfig_story2); 
         auth.delegate({ 
            login: function (callback) { 
               callback(null,{livefyre: '<Login Token>'}); 
            } 
         }); 
      }); 
   </script> 
</body> 
</html>
```
