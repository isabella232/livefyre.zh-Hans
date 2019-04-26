---
description: 在评论流中插入广告。
seo-description: 在评论流中插入广告。
seo-title: 评论中的广告
solution: Experience Manager
title: 评论中的广告
uuid: f8d6372f-4468-4884-a384-116180b4 c748
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 评论中的广告{#ads-in-comments}

在评论流中插入广告。

## 评论中的广告 {#topic_CDD2ACF16AED4DE782725EE90089C04E}

在评论流中插入广告。

“注释”功能中的Livefyre广告允许您插入广告流，定义广告在流中的显示频率，以及创建同步和异步广告注入代表。

Livefyre提供使用广告管理解决方案提供商提供广告的容器。

要插入广告，请传递Livefyre两个值：

* 广告应插入评论流的频率
* 提供相应广告的函数。

>[!NOTE]
>
>只有当广告投放位于视区中时，广告才会呈现。广告仅在父评论之后(不在线程内)显示，用户将无法评论这些广告。此API不允许您指定广告将被放置到的元素的大小。

## 集成 {#concept_C99029E618EC49779E3117D2C303E4F1}

要使用此功能，请在要放置广告的页面上创建div元素，然后从广告提供商处传递HTML。

Livefyre提供两种广告投放类型：同步和异步。这两种类型仅在用户滚动页面时加载广告，使广告的位置处于视图状态。两者还要求您返回DOM元素(iFrame或div)。

要获得广告，同步方法调用到本地存储库，而异步调用外部服务。

### 同步

要创建同步位置，请在委托中包括广告，并返回广告元素本身。同步方法调用到本地存储库，允许您处理自己的广告生成。

### 异步

异步方法要求在调用广告提供者之前将元素插入DOM中。然后，您的提供商决定要发送哪个广告，并将其返回。

要实施异步广告，请创建一个代表将放置广告的元素的委托，以及一个将执行广告放置的回调。委托中返回的元素必须具有指向目标的唯一ID。回调会将广告插入到由唯一ID提供的元素中。

>[!NOTE]
>
>根据广告提供商的不同，回调将行为不同。

加载页面时，注释中的广告将点击委托，注入元素，然后调用回调以更新(以前定义)包含广告的元素。

## 参数 {#concept_D7E27B0C21EF405C8EB826083DBB53EC}

可通过此调用使用以下参数。

对于广告对象：

* **延迟：****(可选)整数** -设置将在其后显示第一个广告的注释数。默认值为10。
* **频率：(可选)整数** -设置随后每个广告都将显示的注释数。例如：输入2，以显示每个评论的广告。默认值为10。
* **委托：*****必需* 函数** -调用广告流中的广告的函数。

委托对象支持同步和异步广告调用。向委托函数(数据)提供的参数将包含：

* **title：****字符串** -集合的标题。
* **标记：****数组** -与集合关联的标记的列表。
* **id：****字符串** -集合的文章标识符。
* **url：****字符串** -集合的URL。
* **DetailBridge：****字符串** -集合的网络ID。
* **siteID：****int** -集合的站点ID。

这些项目通过我们示例中的ConferConfig对象传递， [在“入门”](/help/implementation/c-app-integrations/c-comments-integration/c-comments-integration.md#section_656AAC97903F485084650269A6C7EBCE) 部分中详细介绍了这些项目。

### 同步

委托返回一个对象，其中包含：

* **元素：*****必需* DOM元素** -包含要插入应用程序的广告的元素。

**异步**：委托返回一个对象，其中包含：委托返回一个包含两个属性的对象：元素和回调：

* **元素：*****必需* DOM元素** -包含要插入应用程序的广告的元素。
* **回调：*****必需* 函数** -将处理广告插入到DOM元素中的回调。

对于该 `Conv` 对象，您可以传入一个字符串以表示广告部分的标题：

* **字符串：****(可选)** -用于自定义广告的标题文本。默认情况下，“赞助方”。

## 同步示例 {#concept_E733E4431D9948638B8102ADE398735F}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```

## 异步示例 {#concept_16B798C7EB20423DAA53ACCC71540051}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  function insertSlot(slotName) { 
    var adElem = document.createElement("img"); 
    var ad = "https://your-ad-here.com/great-ad-image.image"; 
    adElem.setAttribute("src", ad); 
    document.getElementById(slotName).appendChild(adElem); 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem, 
              callback: function() { 
                insertSlot(elem.id); 
              } 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```
