---
description: 'null'
seo-description: 'null'
seo-title: 向页面添加指示符
solution: Experience Manager
title: 向页面添加指示符
uuid: 6499c45a-3773-4adb-a6c7-22a628309afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# 向页面添加指示符 {#adding-sidenotes-to-a-page}

Livefyre提供了多个配置选项，用于将Siestrop定位到您的页面上：

* “选择器”选项定义了Sideras应显示的元素。
* 锚点表示可表示的元素。
* 自定义线程容器允许您定义指示线程相对于所指示内容的位置。
* “Sidesork计数”选项允许您显示在给定位置添加的Sidesork数。
* 使用多个 `ConvConfig` 对象将指示符添加到单个页面上的多篇文章。

## 选择器 {#section_wyj_4sv_sy}

选择器选项使Sidesor能够查找页面上的内容。 此选项的值允许您动态确定将使用的元素。 它可以是选择器字符串（如“#content p, #content img”）、jQuery对象(如 `$(‘#content’)`)、DOM元素数组或具有两个属性的对象：包括和排除。 随后，指示应用程序将使用页面上的指定元素或匹配元素。 如果使用include和exclude属性，则Sidestrov将首先解析页面以查找include属性上的所有元素，然后删除在exclude属性上找到的所有元素。

## 锚点 {#section_ehq_psv_sy}

锚点表示其内容可以指示的元素。 锚点元素可以包含文本或图像。 应用程序构建过程中传递的选择器选项将确定锚点元素。

## 锚点ID {#section_rsb_rsv_sy}

页面上的锚点使用 `data-lf-anchor-id`。

要自行设置锚点的ID，请将属 `data-lf-custom-anchor-id` 性添加到要映射到锚点的元素。 当锚点的自动检测失败时，这非常有用。

例如，如果您计划对图像的桌面和移动版本使用不同的URL，则两个不同的URL可能会映射到不同的锚点。 相反，如果HTML在移动和桌 `data-lf-custom-anchor-id` 面上提供的内容相同，则图像元素将被视为单个锚点。

锚点的类型是动态确定的，但也可以使用属性显式设置 `data-lf-custom-anchor-type` 类型。

>[!NOTE]
>
>必须使用枚举编号值。

可用类型包括：

* **** 文本：1
* **** 图像：2
* **** 媒体：3
* **** 丰富：4

有关如 [何使用方法将Sitexer内容动态添加到页](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md)`updateAnchors` 面的更多信息，请参阅updateAnchors方法。

## 自定义线程容器 {#section_jdh_btv_sy}

使用选 `threadContainerEl` 项可指定“指示”线程的位置，而不是默认位置。 默认情况下，当锚点被激活时，指示器将显示在相关内容旁边或下方。 要更改此默认值，请 `threadContainerEl` 使用指定线程应显示的元素。

此选项的此值与选择器选项的工作方式相同，只是使用第一个有效元素。

## Sidesk计数 {#section_pld_ntv_sy}

使用该选 `numSidenotesEl` 项在您的页面上嵌入一个可选的Sidesork计数构件。 此选项接受与选择器选项相同的输入，但将仅使用输入数组中的第一个有效元素。

构件将装饰提供或匹配的元素，并将包括Sidesr输入图标、在此位置输入的Sidesr数量和帮助图标。

单击构件将显示一个快显窗口，其中简要说明了“指示”以及如何使用这些指示。

说明和示例文本都可使用自定义字符串( `questionExplanation` 和 `questionMockText`分别)进行配置。 计数构件和弹出窗口的外观也可以使用自定义样式( `numSidenotes` 和 `numSidenotesPopover`分别)配置。

## 添加多个站点表示集合到单个页面 {#section_pjl_ptv_sy}

Livefyre允许您向单个页面添加多个Sidesort集合。 例如，如果页面包含三则新闻，您可能希望包含三个单独的Sidesorf应用程序小版本。 为此，您必须为要构建的Sideram的每个 `ConvConfig` 实例定义一个单独的对象。 例如：

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
