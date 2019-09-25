---
description: 'null'
seo-description: 'null'
seo-title: Livefyre Analytics事件
solution: Experience Manager
title: Livefyre Analytics事件
uuid: 4eb5a196-ca33-40f8-a96d-ed46469223de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre Analytics事件 {#livefyre-analytics-events}

## 事件对象定义 {#section_dh1_yhn_pdb}

以下代码定义事件对象中由页面上的分析处理程序接收的字段。

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

## Livefyre Analytics事件和eVar {#section_u3k_tft_mcb}

以下Livefyre事件将映射到使用Report Suite manager在报告中使用的自定义事件。 有关Adobe Analytics中报表包的详细信息，请参阅 [报表包管理器](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)。 有关如何将Livefyre事件与Report Suite manager结合使用的更多信息，请参见 [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb)。

## Livefyre Analytics事件

| 事件 | 描述 |
|---|---|
| 初始化 | 加载至少包含一个Livefyre应用程序的页面时 |
| 载入 | 无论用户视图如何，应用程序在页面上加载的任何时间 |
| 查看 | 当应用程序首次进入视区时。 |
| 帖子 | 每当用户发布评论或内容时，包括：顶级帖子、回复、评论、媒体墙上传 |
| 已发布 | 当帖子成功时。 |
| Twitter_Reply | 用户在Twitter上回复的任何时间 |
| Twitter_Like | 将内容共享到的位置：转推 |
| Livefyre_Like | 任何时候在应用程序中使用Livefyre类似功能 |
| Livefyre_Navice | 每当用户不喜欢直播时， |
| ShareOnPost | 用户随时发布内容并使用“发布时共享”功能 |
| ShareButtonClick | 每当用户单击评论上的共享按钮时 |
| ShareTwitter | 单击“共享到Twitter”时 |
| ShareFacebook | 单击“共享到Facebook”时 |
| ShareURL | 选择／复制“共享到URL”文本区域时。 |
| 扩展回复 | 当用户单击+或展开链接以查看顶级帖子上的所有回复时 |
| 折叠回复 | 当用户单击——或折叠链接以查看顶级帖子上的所有回复时 |
| FlagClick | 每当用户打开标志模态时 |
| FlagSpam | 当用户将内容标记为垃圾信息时 |
| FlagSarove | 当用户将内容标记为不同意 |
| FlagOffensive | 当用户将内容标记为冒犯性时 |
| FlagOffTopic | 当用户将内容标记为关闭主题时 |
| 标记取消 | 用户在提交标记时单击X或“取消” |
| FollowCollection | 随时进行对话（“我对评论感兴趣”） |
| UnfollowCollection | 当取消对话时 |
| 请求更多 | 每当用户在应用程序中加载更多内容时（也需要实现高速） |
| ModalView | 用户单击鼠标以在模态中查看内容 |
| TwitterRetweetClick | 将内容共享到的位置：转推 |
| PostButtonClick | 当用户单击帖子时（“您在想什么？”）按钮 |
| 登录 | 用户登录的任何时间 |
| 注销 | 用户在任何时间注销 |

以下是Livefyre提供的转换变量(eVar)列表。

## 转换变量- eVar

| 事件 | 描述 |
|--- |--- |
| 网络ID | Livefyre中的网络ID/名称 |
| 应用程序 ID | 应用程序的URN |
| 上下文ID | Livefyre中的内容ID |
| 应用程序类型 | Livefyre应用程序类型。 选项: <br><ul><li>实时博客  </li><li> 功能卡</li><li>轮播</li><li>聊天 </li><li>注释</li><li>幻灯片</li><li>地图</li><li>马赛克</li><li>媒体墙</li><li>趋势</li><li>上传按钮</li></ul> |
| 内容类型 | Instagram、Twitter、Facebook、LiveFyre、YouTube等 |

## 更多信息 {#section_b3d_4yl_pdb}

有关本页讨论主题的详细信息，请参阅：

* [Report Suite](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[ManagerDTM](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [规则](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)