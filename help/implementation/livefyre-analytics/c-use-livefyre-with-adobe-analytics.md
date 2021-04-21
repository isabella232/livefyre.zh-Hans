---
description: 'null'
exl-id: a866782d-fca6-48bf-9fb8-5080e396919b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 1%

---

# 将Livefyre与Adobe Analytics和Dynamic Tag Manager(DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}结合使用

设置Adobe Analytics和动态标签管理器(DTM)以收集Livefyre应用程序的数据。

## 第1步：在Adobe Analytics中设置事件{#section_iks_kgd_4cb}

在Adobe Analytics Report Suite Manager中将Livefyre事件映射到一个或多个自定义成功事件。

有关报表包管理器的详细信息，请参阅[报表包管理器](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)。

1. 以管理员用户身份登录Adobe Analytics。
1. 打开Adobe Analytics Admin Report Suite Manager。
1. 创建新的报表包或选择现有报表包。
1. 单击要修改的报表包，编辑报表包，然后导航到&#x200B;**[!UICONTROL Edit Settings > Conversion > Success Events]**。
1. 将Livefyre事件映射到一个或多个自定义成功事件。

## 第2步：设置转换变量

在Adobe Analytics Admin Report Suite Manager中将Livefyre转换变量(eVar)映射到转换变量。 转换变量的作用类似于排序函数，可确定您计划如何识别从Livefyre事件收集的数据。

1. 在报表包管理器中，单击&#x200B;**[!UICONTROL Edit Settings > Conversion > Conversion Variables]**。
1. 选择要使用的自定义转换变量(eVar)，并将其映射到Livefyre转换变量。 要将Livefyre转换变量映射到自定义转换变量，请执行以下操作：
* 启用转换变量
* 命名转换变量
* 为转换变量指定类型
1. 保存自定义转换变量。

## 第3步：使用DTM添加包含Livefyre事件{#section_t15_2hd_4cb}的报表包

将Adobe Analytics添加到DTM以使Analytics正常工作。 为此，请创建新属性和工具，并将包含Livefyre事件的新报表包添加到该属性。 有关DTM的详细信息，请参阅[DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html)。

如果您已经为您使用Livefyre事件设置的报表包设置了属性或工具，则无需执行此步骤。

1. 在DTM中，创建或编辑现有属性。
1. 创建或编辑现有Adobe Analytics工具。
1. 如果现有Adobe Analytics工具不存在，请单击&#x200B;**[!UICONTROL Add a Tool]**按钮。
为工具设置以下参数：

   * 将&#x200B;**[!UICONTROL Tool Type]**&#x200B;设置为&#x200B;**[!UICONTROL Adobe Analytics]**。
   * 启用 **[!UICONTROL Automatic Configuration]**.
   * 启用 **[!UICONTROL Authenticate via Marketing Cloud]**.
1. 在&#x200B;**[!UICONTROL Report Suites]**&#x200B;字段中添加或确认具有Livefyre事件的报表包的名称。

## 第4步：设置页面加载规则以设置分析处理{#section_jfj_j3d_4cb}

设置页面加载规则以拉入所有数据。 页面加载规则允许您在页面加载时记录事件的规则中放置自定义javascript。

>[!NOTE]
>
>请勿使用基于事件的规则或直接呼叫规则。

1. 在DTM中，选择&#x200B;**[!UICONTROL Rules]**&#x200B;选项卡。
1. 单击 **[!UICONTROL Page Load Rules]**.
1. 单击&#x200B;**[!UICONTROL Create New Rule]**&#x200B;按钮。
1. 单击&#x200B;**[!UICONTROL Plus]**&#x200B;按钮，打开&#x200B;**[!UICONTROL Conditions]**&#x200B;部分。
1. 触发规则。 如果要异步延迟或实现规则，请选择&#x200B;**[!UICONTROL DOM Ready]**&#x200B;或&#x200B;**[!UICONTROL Onload]**&#x200B;触发器类型。
1. （可选）添加其他参数以限制显示Livefyre应用程序的页面。 有关其他配置选项的详细信息，请参阅[DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html)。
1. 在&#x200B;**[!UICONTROL Javascript/ Third Party Tags]**&#x200B;下，单击&#x200B;**[!UICONTROL Non-sequential]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL Add New Script]**。
1. 选择&#x200B;**[!UICONTROL Sequential HTML]**&#x200B;作为脚本类型。
1. 将以下脚本添加到代码编辑器中，然后单击&#x200B;**[!UICONTROL Save Code]**。

   以下脚本在加载Livefyre JavaScript后调用`livefyre_analytics`直接调用规则。 下面的脚本示例每400ms检查一次，以查看页面上是否有`livefyre.analytics`。 页面加载后，livefyre.analytics会发出跟踪信息。

   ```
   /** 
   * Poll for Livefyre.analytics object to exist since it gets loaded via the 
   * Livefyre.js JavaScript file. Depending on the timing, this could already 
   * exist or need a little time. 
   */ 
   function pollForAnalytics() {  
   if (Livefyre.analytics) { 
     _satellite.track('livefyre_analytics'); 
       return true; 
     } 
     setTimeout(pollForAnalytics, 400); 
   } 
   setTimeout(pollForAnalytics, 400);
   ```

1. 单击 **[!UICONTROL Save Code]**.
1. 单击 **[!UICONTROL Save Rule]**.

## 第5步：创建直接调用规则以为Livefyre {#section_gvp_b1g_pdb}构建Adobe Analytics映射配置

通过使用自定义事件、DTM中的Adobe Analytics UI字段和数据元素，还有其他方法可在DTM中实现Livefyre。 此文档使用自定义Javascript实现相同效果。

1. 在DTM中，选择&#x200B;**Rules**&#x200B;选项卡，然后单击&#x200B;**Direct Call Rules**。
1. 单击&#x200B;**创建新规则**&#x200B;按钮。
1. 将新规则命名为&#x200B;**Livefyre Analytics**。
1. 展开&#x200B;**conditions**&#x200B;配置区域。
1. 在&#x200B;**字符串**&#x200B;字段中，输入`livefyre_analytics`。
1. 展开“Javascript /第三方标记”部分，然后单击&#x200B;**“添加新脚本**”按钮。
1. 在&#x200B;**标记名称**&#x200B;输入框中输入&#x200B;**Livefyre Analytics Config**。
1. 选择&#x200B;**非顺序Javascript**。
1. 在代码编辑器中输入以下Livefyre配置代码，然后单击&#x200B;**保存代码**&#x200B;按钮。

   ```
   var s = _satellite.getToolsByType('sc')[0].getS(); 
   
   var evarMap = {  
     appId: 'eVar81',  
     appType: 'eVar82' 
   }; 
   
   var eventMap = { 
     FlagCancel: 'event82',  
     FlagClick: 'event82',  
     FlagDisagree: 'event82',  
     FlagOffensive: 'event82',  
     FlagOffTopic: 'event82',  
     FlagSpam: 'event82',  
     Like: 'event82', 
     Load: 'event81',  
     RequestMore: 'event82',  
     ShareButtonClick: 'event82',  
     ShareFacebook: 'event82',  
     ShareOnPostClick: 'event82',  
     ShareTwitter: 'event82',  
     ShareURL: 'event82',  
     SortStream: 'event82',  
     TwitterLikeClick: 'event82', 
     TwitterReplyClick: 'event82',  
     TwitterRetweetClick: 'event82',  
     TwitterUserFollow: 'event82' 
   }; 
   
    function trackLivefyreEvent(data) {  
     var event = eventMap[data.type]; 
     console.log('Track:', data.type, event); 
   
     if (!event) { 
       console.warn(data.type, 'is not mapped   to an event in AA');  
       return; 
     } 
     var vars = ['events'];  
     switch (event) { 
       case 'event82': s.eVar83 = data.type;  
         vars.push('eVar83');  
         break; 
       default: 
     } 
       ['generator', 'evars'].forEach(function (type) {  
       var obj = data[type]; 
       for (var d in obj) { 
         if (obj.hasOwnProperty(d) && evarMap[d]) {  
           s[evarMap[d]] = obj[d];  
           vars.push(evarMap[d]); 
         } 
       } 
     }); 
     s.linkTrackVars = vars.join(',');  
     s.linkTrackEvents = event;  
     s.events = event; 
   
     console.log('linkTrackVars:',  s.linkTrackVars);  
     console.log('linkTrackEvents:',  s.linkTrackEvents);  
     console.log('events:', s.events); 
     s.tl(); 
     } 
     ]
   
     /** 
   ```

   * 为来自Livefyre的所有分析事件添加一个分析处理程序。 对于每个事件，它在全局对象上设置事件，然后调度该数据。

   ```
   */ 
   function addAnalyticsHandler() {  
     Livefyre.analytics.addHandler(function (events) { 
       (events || []).forEach(function (data) {  
         console.log('Event handled:', data.type);  
         trackLivefyreEvent(data); 
       }); 
     }); 
   } 
   addAnalyticsHandler();  
   ```

1. 单击&#x200B;**保存规则**。

## 第6步：批准页面加载规则{#section_pxc_11t_ycb}的更改

1. 转到&#x200B;**[!UICONTROL Approvals]**&#x200B;选项卡。
1. 单击 **[!UICONTROL Approve]**.
1. 单击&#x200B;**[!UICONTROL Yes, approve]**&#x200B;以确认您的批准。
1. 转至 **[!UICONTROL Overview > Publish Queue]**.
1. 选择要发布的规则。
1. 单击 **[!UICONTROL Publish Selected]**.
1. 单击&#x200B;**[!UICONTROL Publish]**&#x200B;确认要发布。

## 脚本 {#section_xkb_vft_mcb}

以下示例代码将特定eVar映射到可用的Livefyre eVar。 Livefyre转换变量(`eVar`)名称（例如`appId`）映射到您在报表包管理器中设置的名称（例如`eVar81`）。 将此脚本中的`eVar`名称更改为自定义转换变量。


```
var s = _satellite.getToolsByType`('sc')[0]`.getS(); 
var evarMap = { 
  appId: 'eVar81', 
  appType: 'eVar82' 
};
```

以下示例代码将您在报表包管理器中设置的特定事件与可用的Livefyre事件映射。 在此示例中，`event82`设置为任何用户交互事件，而不区分哪种用户交互事件（例如，称赞或共享内容）。 这是一种在块中记录所有用户交互信息的有效方法。 您还可以使用数据元素引用在DTM分析UI中映射事件。

```
var eventMap = { 
  FlagCancel: 'event82',  
  FlagClick: 'event82',  
  FlagDisagree: 'event82',  
  FlagOffensive: 'event82',  
  FlagOffTopic: 'event82',  
  FlagSpam: 'event82',  
  Like: 'event82', 
  Load: 'event81',  
  RequestMore: 'event82',  
  ShareButtonClick: 'event82',  
  ShareFacebook: 'event82',  
  ShareOnPostClick: 'event82',  
  ShareTwitter: 'event82',  
  ShareURL: 'event82',  
  SortStream: 'event82',  
  TwitterLikeClick: 'event82', 
  TwitterReplyClick: 'event82',  
  TwitterRetweetClick: 'event82',  
  TwitterUserFollow: 'event82' 
};
```

以下示例说明，如果此列表中没有事件，则不要执行任何操作。 您无需修改此代码部分。

```
function trackLivefyreEvent(data) {  
  var event = eventMap[data.type]; 
  console.log('Track:', data.type, event); 
   
  if (!event) { 
    console.warn(data.type, 'is not mapped to an event in AA');  
    return; 
  }
```

以下代码区分了`event82`记录的事件类型。 转换变量`eVar83`记录用户交互的类型，脚本设置`eVar83`以按类型分隔用户交互数据。 因此，`eVar83`允许您将记录的数据分解为特定类型的用户交互。

```
  var vars = ['events'];  
  switch (event) { 
    case 'event82': s.eVar83 = data.type;  
      vars.push('eVar83');  
      break; 
    default: 
  } 
   
  ['generator', 'evars'].forEach(function (type) {  
    var obj = data[type]; 
    for (var d in obj) { 
      if (obj.hasOwnProperty(d) && evarMap[d]) {  
        s[evarMap[d]] = obj[d];  
        vars.push(evarMap[d]); 
      } 
    } 
  }); 
   
  s.linkTrackVars = vars.join(',');  
  s.linkTrackEvents = event;  
  s.events = event; 
   
  console.log('linkTrackVars:', s.linkTrackVars);  
  console.log('linkTrackEvents:', s.linkTrackEvents);  
  console.log('events:', s.events); 
   
  s.tl(); 
}
```

下面的代码示例添加一个处理函数来侦听发生的所有事件。 它在加载时使用页面加载规则，等待事件存在，然后为应用程序中的所有事件设置处理程序并跟踪它们。 您无需修改此代码。

```
/** 
* Adds an analytics handler for all analytics events from Livefyre. For each event, it sets the data on a global object and then dispatches the event. 
*/ 
function addAnalyticsHandler() { 
  Livefyre.analytics.addHandler(function (events) { 
    (events || []).forEach(function (data) { 
      console.log('Event handled:', data.type); 
      trackLivefyreEvent(data); 
    }); 
  }); 
}
```

## 更多信息

有关本页讨论的主题的详细信息，请参阅：

* [报表包管理器](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)
* [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html)
* [规则](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
