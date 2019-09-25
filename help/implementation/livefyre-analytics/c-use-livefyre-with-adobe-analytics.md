---
description: 'null'
seo-description: 'null'
seo-title: 将Livefyre与Adobe Analytics和Dynamic Tag Manager(DTM)lk xavvn Vefyre结合使用，与Adobe Analytics和Dynamic Tag Manager(DTM)结合使用
uuid: 9a1c25c0-c474-46ff-82ac-e89357007c7f
translation-type: tm+mt
source-git-commit: 55bfc0a545bb4a1093c29bd11e764c9799135324

---


# 将Livefyre与Adobe Analytics和Dynamic Tag Manager(DTM)结合使用{#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

设置Adobe Analytics和Dynamic Tag Manager(DTM)以收集Livefyre应用程序的数据。

## 第1步：在Adobe Analytics中设置事件 {#section_iks_kgd_4cb}

将Livefyre事件映射到Adobe Analytics Report Suite manager中的一个或多个自定义成功事件。

有关“报告套件管理器”的详细信息，请参阅 [报告套件管理器](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)。

1. 以管理员用户身份登录到Adobe Analytics。
1. 打开Adobe Analytics Admin Report Suite Manager。
1. 创建新的报表包或选择现有报表包。
1. 通过单击要修改的报表包来编辑报表包，然后导航到 **[!UICONTROL Edit Settings > Conversion > Success Events]**。
1. 将Livefyre事件映射到一个或多个自定义成功事件。

## 第2步：设置转换变量

将Livefyre转化变量(eVar)映射到Adobe Analytics Admin Report Suite manager中的转化变量。 转换变量的作用类似于排序函数，可确定您计划如何识别从Livefyre事件收集的数据。

1. 在“报表包管理器”中，单击 **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**。
1. 选择要使用的自定义转换变量(eVar)并将其映射到Livefyre转换变量。 要将Livefyre转换变量映射到自定义转换变量，请执行以下操作：
* 启用转换变量
* 命名转换变量
* 为转换变量指定类型
1. 保存自定义转换变量。

## 第3步：使用DTM添加包含Livefyre事件的报表包 {#section_t15_2hd_4cb}

将Adobe Analytics添加到DTM，使Analytics正常工作。 为此，请创建一个新属性和工具，并将包含Livefyre事件的新报表包添加到该属性中。 有关DTM的详细信息，请参 [阅DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)。

如果您已经为使用Livefyre事件设置的报表包设置了属性或工具，则无需执行此步骤。

1. 在DTM中，创建或编辑现有属性。
1. 创建或编辑现有Adobe Analytics工具。
1. 如果现有Adobe Analytics工具不存在，请单击该 **[!UICONTROL Add a Tool]** 按钮。
为工具设置以下参数：
* Set **[!UICONTROL Tool Type]** to **[!UICONTROL Adobe Analytics]**.
* Enable **[!UICONTROL Automatic Configuration]**.
* Enable **[!UICONTROL Authenticate via Marketing Cloud]**.
1. 在字段中添加或确认包含Livefyre事件的报表包的名 **[!UICONTROL Report Suites]** 称。

## 第4步：设置页面加载规则以设置分析处理 {#section_jfj_j3d_4cb}

设置页面加载规则以拉入所有数据。 页面加载规则允许您在页面加载时将自定义javascript放入记录事件的规则中。

>[!NOTE]
>
>请勿使用基于事件的规则或直接调用规则。

1. 在DTM中，选择选 **[!UICONTROL Rules]** 项卡。
1. 单击 **[!UICONTROL Page Load Rules]**.
1. 单击该按 **[!UICONTROL Create New Rule]** 钮。
1. 通过单 **[!UICONTROL Conditions]** 击按钮打开该部 **[!UICONTROL Plus]** 分。
1. 触发规则。 如果 **[!UICONTROL DOM Ready]** 要 **[!UICONTROL Onload]** 异步延迟或实现规则，请选择或触发类型。
1. （可选）添加其他参数以限制显示Livefyre应用程序的页面。 有关其他配置选项的详细信息，请参 [阅DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)。
1. 在下 **[!UICONTROL Javascript/ Third Party Tags]**&#x200B;面，单击 **[!UICONTROL Non-sequential]** 选项卡，然后单击 **[!UICONTROL Add New Script]**。
1. 选择 **[!UICONTROL Sequential HTML]** 作为脚本类型。
1. 将以下脚本添加到代码编辑器中，然后单击 **[!UICONTROL Save Code]**。
以下脚本在Livefyre javaScript `livefyre_analytics` 加载后调用直接调用规则。 以下脚本示例每400毫秒检查一次，以查 `livefyre.analytics` 看页面上是否存在。 页面加载后，livefyre.analytics会发出跟踪信息。

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

## 第5步：创建直接调用规则，为Livefyre构建Adobe Analytics映射配置 {#section_gvp_b1g_pdb}

使用自定义事件、DTM中的Adobe Analytics UI字段和数据元素，还有其他方法在DTM中实现Livefyre。 本文档使用自定义Javascript实现相同的效果。

1. 在DTM中，选择“ **规则** ”选项卡，然后单击“ **直接调用规则”**。
1. Click on the **Create New Rule** button.
1. 将新规则命名为 **Livefyre Analytics**。
1. 展开条 **件配置** 区域。
1. 在“字 **符串** ”字段中，输入 `livefyre_analytics`。
1. 展开“Javascript /第三方标记”部分，然后单击“添 **加新脚本** ”按钮。
1. 在“ **标记名称** ”输入框 **中输入Livefyre Analytics** Config。
1. Select **Non-Sequential Javascript**.
1. 在代码编辑器中输入以下Livefyre配置代码，然后单击“保 **存代码** ”按钮。

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

* Adds an analytics handler for all analytics events from Livefyre. For each event, it sets the data on a global object and then dispatches the event.

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

var s = _satellite.getToolsByType`('sc')[0]`.getS();
var evarMap = {
appId: 'eVar81',
appType: 'eVar82'
};

```
The following sample code maps the specific events you set up in the Report Suite Manager with available Livefyre events. In this example, `event82` is set up as any user interaction event without differentiating which kind of user interaction event (for example, liking or sharing content). This is an efficient way to record all user interaction information in a block. You can also map the events in the DTM Analytics UI with Data Element referencing.
```

var eventMap = {FlagCancel:'event82',\
标记单击：'event82',\
旗标反对：'event82',\
旗帜进攻：'event82',\
FlagOffTopic:'event82',\
FlagSpam:'event82',\
喜欢：'event82'，加载：'event81',\
RequestMore: 'event82',\
ShareButtonClick:'event82',\
ShareFacebook: 'event82',\
ShareOnPostClick:'event82',\
ShareTwitter:'event82',\
ShareURL:'event82',\
SortStream:'event82',\
TwitterLikeClick:'event82',TwitterReplyClick:'event82',\
TwitterRetweetClick:'event82',\
TwitterUserFollow:'event82'};

```
The following sample states that if there isn't an event in this list, don't do anything. You do not need to modify this section of code.
```

function trackLivefyreEvent(data){\
var event =[eventMapdata.type];console.log('Track:', data.type, event);

if(!event){console.warn(data.type, 'is not mapped to a event in AA');\
返回；}

```
The following code differentiates the event types that `event82` records. The conversion variable, `eVar83` records the type of user interaction, and the script sets up `eVar83` to separate the user interaction data by type. So `eVar83` allows you to break out the recorded data into specific types of user interactions.
```

var vars = ['events];\
switch(event){case 'event82':s.eVar83 = data.type;\
vars.push('eVar83');\
休息；默认：}

['generator', 'evars'].forEach(function(type){\
var obj =[datatype];for(var d in obj){if(obj.hasOwnProperty(d)&amp;&amp;[evarMapd]){\
s[[evarMapd]] =[objd];\
vars.push([evarMapd]);}});

s.linkTrackVars = vars.join(',');\
s.linkTrackEvents = event;\
s.events = event;

console.log('linkTrackVars:', s.linkTrackVars);\
console.log('linkTrackEvents:', s.linkTrackEvents);\
console.log('events:', s.events);

s.tl();
}

```
The following code sample adds a handler to listen to all the events that happen. It uses the page load rule on load, waits for events to exist, then sets up handler for all events from the App and tracks them. You do not need to modify this code.
```

/**
* 为来自Livefyre的所有分析事件添加一个分析处理程序。 对于每个事件，它在全局对象上设置数据，然后调度该事件。

*/function addAnalyticsHandler(){Livefyre.analytics.addHandler(function(events){(events)|| [])。forEach(function(data){console.log('Event handled:', data.type);trackLivefyreEvent(data);});});}

```
## More Info

For more information on the topics discussed on this page, see:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Rules](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)

