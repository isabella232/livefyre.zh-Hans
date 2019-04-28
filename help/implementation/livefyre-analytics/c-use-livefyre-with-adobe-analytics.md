---
description: 'null'
seo-description: 'null'
seo-title: 使用Adobe Analytics和Dynamic Tag Manager(DTM)将Livefyre与Adobe Analytics和Dynamic Tag Manager(DTM) lk xavvn vefyre结合使用
uuid: a1c25c0-c474-46ff-82ac-e89357007 c7 f
translation-type: tm+mt
source-git-commit: 55bfc0a545bb4a1093c29bd11e764c9799135324

---


# 将Livefyre与Adobe Analytics和Dynamic Tag Manager(DTM)结合使用{#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

设置Adobe Analytics和Dynamic Tag Manager(DTM)以收集Livefyre应用程序的数据。

## 步骤1：在Adobe Analytics中设置活动 {#section_iks_kgd_4cb}

在Adobe Analytics Report Suite Manager中将Livefyre事件映射到一个或多个自定义成功事件。

有关报告套件管理器的详细信息，请参阅 [报告套件管理器](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)。

1. 以管理员用户身份登录Adobe Analytics。
1. 打开Adobe Analytics管理员报告套件管理器。
1. 创建新的报表包或选择现有报表包。
1. 单击要修改的报表包，然后导航到 **[!UICONTROL Edit Settings > Conversion > Success Events]**该报表包，以编辑报表包。
1. 将Livefyre事件映射到一个或多个自定义成功事件。

## 步骤2：设置转换变量

在Adobe Analytics管理员报告套件管理器中将Livefyre转换变量(eVar)映射到转化变量。转换变量的行为类似于排序函数，用于确定您计划如何识别从Livefyre事件收集的数据。

1. 在Report Suite Manager中单击 **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**。
1. 选择自定义转化变量(eVar)以使用并将其映射到Livefyre转换变量。要将Livefyre转换变量映射到自定义转换变量，请执行以下操作：
* 启用转换变量
* 命名转换变量
* 为转换变量提供类型
1. 保存自定义转换变量。

## 步骤3：使用DTM添加带有Livefyre Events的报表包 {#section_t15_2hd_4cb}

将Adobe Analytics添加到DTM以获得Analytics工作。为此，请创建一个新的属性和工具，并将带有Livefyre事件的新报表包添加到该属性。有关DTM的详细信息，请参阅 [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)。

如果已经为设置了Livefyre事件的报表包设置了属性或工具，则无需执行此步骤。

1. 在DTM中，创建或编辑现有属性。
1. 创建或编辑现有Adobe Analytics工具。
1. 如果现有Adobe Analytics工具不存在，请单击 **[!UICONTROL Add a Tool]** 按钮。
为工具设置以下参数：
* 设置 **[!UICONTROL Tool Type]****[!UICONTROL Adobe Analytics]**为。
* 启用 **[!UICONTROL Automatic Configuration]**。
* 启用 **[!UICONTROL Authenticate via Marketing Cloud]**。
1. 向 **[!UICONTROL Report Suites]** 字段添加或确认带有Livefyre事件的报表包的名称。

## 第步：设置页面加载规则设置分析处理 {#section_jfj_j3d_4cb}

设置页面加载规则以拖入所有数据。页面加载规则允许您在规则中放置自定义javascript，该规则在加载页面时记录活动。

>[!NOTE]
>
>请勿使用基于事件的规则或直接呼叫规则。

1. 在DTM中，选择 **[!UICONTROL Rules]** 选项卡。
1. 单击 **[!UICONTROL Page Load Rules]**。
1. 单击 **[!UICONTROL Create New Rule]** 按钮。
1. 单击按钮以打开 **[!UICONTROL Conditions]** 章节 **[!UICONTROL Plus]** 。
1. 触发规则。如果 **[!UICONTROL DOM Ready]** 要延迟或以异步方式实施规则，请选择 **[!UICONTROL Onload]** 或触发类型。
1. (可选)添加其他参数以限制显示Livefyre应用程序的页面。有关其他配置选项的更多信息，请参阅 [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)。
1. 下 **[!UICONTROL Javascript/ Third Party Tags]**，单击 **[!UICONTROL Non-sequential]** 选项卡，然后单击 **[!UICONTROL Add New Script]**。
1. 选择 **[!UICONTROL Sequential HTML]** 作为脚本类型。
1. 在代码编辑器中添加以下脚本，然后单击 **[!UICONTROL Save Code]**。
以下脚本在Livefyre JavaScript加载后调用 `livefyre_analytics` 直接调用规则。以下脚本示例每隔400毫秒检查一次是否 `livefyre.analytics` 在页面上。加载页面后，livefyre会发出跟踪信息。

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

1. 单击 **[!UICONTROL Save Code]**。
1. 单击 **[!UICONTROL Save Rule]**。

## 第步：创建直接调用规则以构建Livefyre的Adobe Analytics映射配置 {#section_gvp_b1g_pdb}

通过使用自定义事件、DTM中的Adobe Analytics UI字段以及数据元素，还可以通过其他方式实施Livefyre。本文档使用自定义Javascript实现相同的效果。

1. 在DTM中，选择 **规则** 选项卡，然后单击 **直接调用规则**。
1. 单击 **创建新规则** 按钮。
1. 命名新规则 **Livefyre Analytics**。
1. 展开 **条件** 配置区域。
1. 在 **“字符串** ”字段中，输入 `livefyre_analytics`。
1. 展开Javascript/第方标记部分，然后单击 **添加新脚本** 按钮。
1. 在“标记名称”输入框中输入 **Livefyre** **Analytics** Config。
1. 选择 **非顺序Javascript**。
1. 在代码编辑器中输入以下Livefyre配置代码，然后单击 **“保存代码** ”按钮。

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

* 为Livefyre中的所有分析事件添加分析处理程序。对于每个事件，它将数据设置在全局对象上，然后调度事件。

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
1. Click on **Save Rule**.

## Step 6: Approve changes for Page Load Rule {#section_pxc_11t_ycb}

1. Go to **[!UICONTROL Approvals]** tab.
1. Click **[!UICONTROL Approve]**.
1. Click **[!UICONTROL Yes, approve]** to confirm your approval.
1. Go to **[!UICONTROL Overview > Publish Queue]**.
1. Select the Rule to publish.
1. Click **[!UICONTROL Publish Selected]**.
1. Click **[!UICONTROL Publish]** to confirm that you want to publish.

## Script {#section_xkb_vft_mcb}

The following sample code maps the specific eVars to available Livefyre eVars. The Livefyre conversion variable ( `eVar`) name (for example, `appId`) maps to the name you set up in the Report Suite Manager (for example, `eVar81`). Change the `eVar` names in this script to the custom conversion variables.
```

var s=_ satellite. getToolsByType`('sc')[0]`. Gets()；
var eVarp={appID：&#39;eVar81&#39;，appType：&#39;eVar82&#39;}；

```
The following sample code maps the specific events you set up in the Report Suite Manager with available Livefyre events. In this example, `event82` is set up as any user interaction event without differentiating which kind of user interaction event (for example, liking or sharing content). This is an efficient way to record all user interaction information in a block. You can also map the events in the DTM Analytics UI with Data Element referencing.
```

var eventMap={FlagCancel：&#39;event82&#39;，\
FlagClick：&#39;event82&#39;，\
旗标同意：&#39;event82&#39;，\
Flagpackagy：&#39;event82&#39;，\
标记主题：&#39;event82&#39;，\
标记垃圾邮件：&#39;event82&#39;，\
如：&#39;event82&#39;，加载：“event81”，\
请求更多：&#39;event82&#39;，\
ShareButtonClick：&#39;event82&#39;，\
ShareFacebook：&#39;event82&#39;，\
ShareOnPostClick：&#39;event82&#39;，\
ShareTwitter：&#39;event82&#39;，\
ShareURL：&#39;event82&#39;，\
SortStream：&#39;event82&#39;，\
TwitterLikeClick：“event82”，TwitterReplicCyclick：&#39;event82&#39;，\
TwitterretweetClick：&#39;event82&#39;，\
TwitterUser追随：&#39;event82&#39;}；

```
The following sample states that if there isn't an event in this list, don't do anything. You do not need to modify this section of code.
```

function trackLivefyReEvent(数据){\
var event= eventMapData[. type]；
console. log(&#39;Track：&#39;，data. type，event)；

if(！event){console.
warning(data. type，&#39;未映射到AA&#39;中的事件)；\
return；}

```
The following code differentiates the event types that `event82` records. The conversion variable, `eVar83` records the type of user interaction, and the script sets up `eVar83` to separate the user interaction data by type. So `eVar83` allows you to break out the recorded data into specific types of user interactions.
```

var vars= [&#39;events&#39;]；\
switch(event){case&#39;event82&#39;：s. eVar83= data. type；\
vars. push(&#39;eVar83&#39;)；\
break；
默认：}

[“generator”，&#39;evars&#39;].for每每种(函数(类型){\
var obj= datatype[]；
for(var d in obj){if(obj.
hasownProperty(d)&amp; eeArmapD[]){if\
s[eVARMAPD[]]= objd[]；\
vars. push(eVARMAPD[])；}}})；

s. linkTrackVars= vars. join(&#39;，&#39;)；\
s. linkTrackEvents= event；\
s. events= event；

console. log(&#39;linkTrackVars：&#39;，s. linkTrackVars)；\
console. log(&#39;linkTrackEvents：&#39;，s. linkTrackEvents)；\
console. log(&#39;event：&#39;，s. events)；

s. tl()；}

```
The following code sample adds a handler to listen to all the events that happen. It uses the page load rule on load, waits for events to exist, then sets up handler for all events from the App and tracks them. You do not need to modify this code.
```

/**
* 为Livefyre中的所有分析事件添加分析处理程序。对于每个事件，它将数据设置在全局对象上，然后调度事件。

*/function addAnalyticsHandler(){Livefyre.
analytics. addHandler(function){(events){(events)|||| []).for每每个(函数(数据){console.
log(&#39;事件已处理&#39;：&#39;，data. type)；
trackLiveFyReEvent(data)；})；})；})

```
## More Info

For more information on the topics discussed on this page, see:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Rules](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)

