---
description: 'null'
seo-description: 'null'
seo-title: Livefyre Analytics事件
solution: Experience Manager
title: Livefyre Analytics事件
uuid: eb5a196-ca33-40f8-a96 d-ed46469223 de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre Analytics事件 {#livefyre-analytics-events}

## 活动对象定义 {#section_dh1_yhn_pdb}

以下代码定义在页面上由分析处理函数接收的事件对象中的字段。

```
{
  evars: {
    appId : string : URN ID of the app
    appType : string : Type of the app
    contentType : string : Type of the content that this event pertains to
    contextId : string : URN ID of the contextual item that this event pertains to
    environment : string : Environment that this app is using
    networkId : string : Network that this app is using
    publishedDate : number : Epoch time when the app was published
    userLoggedIn : boolean : If a user is logged in
  },
  generator: {
    env : string: Environment that this app is using
    id : string: URN ID of the app
    name : string: Name of the app
    networkId : string: Network that this app is using
    source : string: URN of the collection
    version : string: Semver version of the app
  },
  startTime : number: Epoch time when event was created
  type : string: Event type (Table 1)
}
```

## Livefyre Analytics Events和eVar {#section_u3k_tft_mcb}

以下Livefyre事件，用于映射到使用Report Suite管理器在报表中使用的自定义事件。有关Adobe Analytics中报表包的更多信息，请参阅 [报告套件管理器](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)。有关如何使用Report Suite Manager使用Livefyre事件的更多 [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb)信息，请参阅。

## Livefyre Analytics事件

| Event | 描述 |
|---|---|
| Init | 当包含至少一个Livefyre应用程序的页面加载时 |
| Load | 无论用户视图如何，均可在页面上加载应用程序 |
| View | 应用程序首次进入viewport时。 |
| Post | 任何时候用户发布评论或内容包括ex：顶级帖子、回复、审阅、媒体墙上传 |
| 已发布 | 当帖子成功时。 |
| Twitter_回复 | 任何时候用户在Twitter上回复 |
| Twitter_赞 | 将内容共享到：转推 |
| Livefyre_ Like | 任何时间livefyre类似于应用程序中的 |
| Livefyre_不同 | 任何时候用户不喜欢livefyre |
| ShareOnPost | 每当用户发布帖子内容并在帖子功能上使用共享时 |
| ShareButtonClick | 每当用户单击注释上的共享按钮时 |
| ShareTwitter | 当单击共享到Twitter时 |
| ShareFacebook | 当单击共享到Facebook时 |
| ShareUrl | 当选择/复制“共享到URL”文本区域时。 |
| ExpandReadies | 当用户单击+或展开链接以查看顶级帖子上的所有回复时 |
| CollapsePLies | 用户单击-或折叠链接时，查看顶级帖子上的所有回复 |
| FlagClick | 任何时候用户均可打开标记Modal |
| Flagspam | 当用户将内容标记为垃圾信息时 |
| 标记同意 | 用户将内容标记为不同意时 |
| Flagpockager | 当用户将内容标记为冒犯性时 |
| 标记主题 | 当用户将内容标记为关闭主题时 |
| FlagCancel | 用户在提交旗标时随时单击X或“取消” |
| followCollection | 任何时候都会进行对话(“我对此感兴趣”) |
| UnfollowCollection | 当对话未遵循 |
| 请求更多 | 每当用户在应用程序中加载更多内容时(需要高速传输) |
| ModalView | 每当用户单击以查看模态中的内容时 |
| TwitterRetweetClick | 将内容共享到：转推 |
| PostButtonClick | 当用户单击帖子时(“您想找什么？“)button |
| 登录名 | 任何用户登录的时间 |
| 注销 | 任何用户注销的时间 |

以下是Livefyre提供的转化变量(eVar)列表。

## 转换变量- eVar

| Event | 描述 |
|--- |--- |
| 网络ID | Livefyre中的网络ID/名称 |
| App ID | 应用程序的URN |
| 上下文ID | Livefyre中的内容ID |
| 应用程序类型 | Livefyre App Type。选项： <br><ul><li>Live Blog  </li><li> 功能卡</li><li>Carousel</li><li>聊天 </li><li>注释</li><li>幻灯片</li><li>地图</li><li>Mosaic</li><li>媒体墙</li><li>趋势趋势</li><li>上传按钮</li></ul> |
| 内容类型 | Instagram、Twitter、Facebook、Livefyre、YouTube等 |

## 更多信息 {#section_b3d_4yl_pdb}

有关此页面上讨论的主题的详细信息，请参阅：

* [Report Suite ManagerDTM](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [规则](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre. js](/help/implementation/c-livefyre.js.md)