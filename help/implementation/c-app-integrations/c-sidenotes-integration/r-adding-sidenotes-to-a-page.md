---
title: 向页面添加指示符
description: 向页面添加指示符
exl-id: 3ec089d0-3d51-4918-b510-d30ef645c9c2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# 向页面{#adding-sidenotes-to-a-page}添加Siestror

Livefyre提供了多个配置选项，用于在您的页面上定位Siestr:

* “选择器”选项定义应显示Siderf的元素。
* 锚点表示可表示的元素。
* 自定义线程容器允许您定义“指示线程”相对于所指示内容的位置。
* “表示计数”选项允许您显示在给定位置添加的表示数。
* 使用多个`ConvConfig`对象将Siestor添加到单个页面上的多篇文章。

## 选择器{#section_wyj_4sv_sy}

选择器选项使Siestrator能够查找页面上的内容。 此选项的值允许您动态确定将使用的元素。 它可以是选择器字符串(如“#content p， #content img”)、jQuery对象（如`$(‘#content’)`）、DOM元素数组或具有两个属性的对象：包括和排除。 随后，指示应用程序将使用页面上指定的元素或匹配的元素。 如果使用include和exclude属性，则Sidestr将首先分析页面以查找include属性上的所有元素，然后删除exclude属性上找到的所有元素。

## 锚点{#section_ehq_psv_sy}

锚点表示可指示其内容的元素。 锚点元素可以包含文本或图像。 应用程序构建过程中传递的选择器选项将确定锚点元素。

## 锚点ID {#section_rsb_rsv_sy}

页面上的锚点使用`data-lf-anchor-id`进行标识。

要自行设置锚点的ID，请将属性`data-lf-custom-anchor-id`添加到要映射到锚点的元素。 当锚点自动检测失败时，此功能非常有用。

例如，如果您计划对图像的桌面版本和移动版本使用不同的URL，则两个不同的URL可能会映射到不同的锚点。 相反，如果您的HTML在移动设备和桌面上提供相同的`data-lf-custom-anchor-id`，则图像元素将被视为单个锚点。

锚具有动态确定的类型，但也可以使用`data-lf-custom-anchor-type`属性显式设置。

>[!NOTE]
>
>必须使用明细列表编号值。

可用类型有：

* **文本：** 1
* **图像：** 2
* **媒体：** 3
* **富：** 4

有关如何使用`updateAnchors`方法将Sitexer内容动态添加到页面的详细信息，请参阅[updateAnchors方法](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md)。

## 自定义线程容器{#section_jdh_btv_sy}

使用`threadContainerEl`选项为“指示线程”(Siser)指定位置，而不是默认位置。 默认情况下，激活锚点后，相关内容旁边或下方将显示“指示符”。 要更改此默认值，请使用`threadContainerEl`指定线程应显示的元素。

此选项的此值与选择器选项的工作方式相同，只使用第一个有效元素。

## 表示计数{#section_pld_ntv_sy}

使用`numSidenotesEl`选项在您的页面上嵌入一个可选的Siestor Widget。 此选项接受与选择器选项相同的输入，但将仅使用输入数组中的第一个有效元素。

构件将装饰提供或匹配的元素，并将包括“指示符”输入图标、在此位置输入的“指示符”数量和帮助图标。

单击该构件将显示一个快显窗口，其中简短说明了“指示”以及如何使用这些指示。

说明和示例文本都可以使用自定义字符串（分别为`questionExplanation`和`questionMockText`）进行配置。 计数构件和跨距的外观也可使用自定义样式（分别为`numSidenotes`和`numSidenotesPopover`）进行配置。

## 将多个Sider表示集合添加到单页{#section_pjl_ptv_sy}

Livefyre允许您向单个页面添加多个Siters集合。 例如，如果页面包含三则新闻，您可能希望包含三个单独的小版本的“Siestr App”。 为此，必须为要构建的Siderf的每个实例定义一个单独的`ConvConfig`对象。 例如：

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
