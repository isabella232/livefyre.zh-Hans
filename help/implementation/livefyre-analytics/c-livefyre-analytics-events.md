---
title: Livefyre Analytics事件
description: Livefyre Analytics事件
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
source-git-commit: 53aead87db517e6f68266a66115889509287a287
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 4%

---

# Livefyre Analytics事件

## 事件对象定义 {#section_dh1_yhn_pdb}

以下代码定义页面上的分析处理程序收到的事件对象中的字段。

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

以下Livefyre事件要映射到使用报表包管理器在报表中使用的自定义事件。 有关Adobe Analytics中报表包的更多信息，请参阅[报表包管理器](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)。 有关如何在报表包管理器中使用Livefyre事件的更多信息，请参阅[](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb)。

## Livefyre Analytics事件

| 事件 | 描述 |
|---|---|
| 初始化 | 加载至少包含一个Livefyre应用程序的页面时 |
| 载入 | 无论用户是否查看，每当在页面上加载应用程序时 |
| 查看 | 当应用程序首次进入视区时。 |
| 帖子 | 每当用户发布评论或一段内容时，包括：顶级帖子、回复、评论、媒体涂鸦墙上传 |
| 已发布 | 帖子成功时。 |
| Twitter_Reply | 用户在任何时候回复Twitter |
| Twitter_Like | 将内容共享到的位置：转推 |
| Livefyre_Like | 任何时候在应用程序中使用livefyre之类的功能 |
| Livefyre(_N) | 每当用户不喜欢Livefyre时， |
| ShareOnPost | 无论用户何时发布内容并使用在发布时共享功能 |
| ShareButtonClick | 每当用户单击评论上的共享按钮时 |
| ShareTwitter | 单击共享到Twitter时 |
| ShareFacebook | 单击共享到Facebook时 |
| ShareURL | 选择/复制共享到URL文本区域时。 |
| ExpandReplies | 当用户单击+或展开链接以查看顶级帖子上的所有回复时 |
| 折叠回复 | 当用户单击 — 或折叠链接以查看顶级帖子上的所有回复时 |
| FlagClick | 用户随时打开标志模式窗口 |
| FlagSpam | 用户将内容标记为垃圾信息时 |
| FlagAdobe | 用户将内容标记为不同意时 |
| 旗帜进攻 | 用户将内容标记为冒犯时 |
| FlagOffTopic | 用户将内容标记为关闭主题时 |
| 标记取消 | 用户在提交标记时随时单击X或“取消” |
| FollowCollection | 每次进行对话后（“我对评论感兴趣”） |
| UnfollowCollection | 取消对话后 |
| 请求更多 | 每当用户在应用程序中加载更多内容时（也需要高速加载） |
| ModalView | 用户单击以在模式中查看内容的任何时间 |
| TwitterRetweetClick | 将内容共享到的位置：转推 |
| PostButtonClick | 当用户点击帖子（“您在想什么？”）时 按钮 |
| 登录 | 用户在任何时候登录 |
| 注销 | 用户在任何时候注销 |

以下是Livefyre提供的转化变量(eVar)列表。

## 转化变量 — eVar

| 事件 | 描述 |
|--- |--- |
| 网络ID | Livefyre中的网络ID/名称 |
| 应用程序 ID | 应用程序的URN |
| 上下文ID | Livefyre中的内容ID |
| 应用程序类型 | Livefyre应用程序类型。 选项: <br><ul><li>实时博客  </li><li> 功能卡</li><li>轮播</li><li>聊天 </li><li>注释</li><li>Filmstrip</li><li>地图</li><li>马赛克</li><li>媒体墙</li><li>趋势</li><li>上传按钮</li></ul> |
| 内容类型 | Instagram、Twitter、Facebook、LiveFyre、YouTube等 |

## 更多信息 {#section_b3d_4yl_pdb}

有关本页所讨论主题的更多信息，请参阅：

* [报表包管](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)[理器DTM](https://experienceleague.adobe.com/docs/livefyre/using/apps/filmstrip/c-filmstrip-app.html?lang=en)

* [规则](https://experienceleague.adobe.com/docs/dtm/using/resources/rules/create-rules.html?lang=en)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
