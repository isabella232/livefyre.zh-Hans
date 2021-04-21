---
title: Livefyre Analytics事件
description: Livefyre Analytics事件
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 4%

---

# Livefyre Analytics事件

## 事件对象定义{#section_dh1_yhn_pdb}

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

以下Livefyre事件将映射到自定义事件，以便在使用报表包管理器的报表中使用。 有关Adobe Analytics中报表包的详细信息，请参阅[报表包管理器](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)。 有关如何将Livefyre事件与Report Suite Manager结合使用的详细信息，请参阅[](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb)。

## Livefyre Analytics事件

| 事件 | 描述 |
|---|---|
| 初始化 | 加载至少包含一个Livefyre应用程序的页面时 |
| 载入 | 任何时候，无论用户视图如何，应用程序都会加载到页面上 |
| 查看 | 应用程序首次进入视区时。 |
| 帖子 | 用户每次发布评论或内容时，包括：顶级帖子、回复、评论、媒体墙上传 |
| 已发布 | 当帖子成功时。 |
| Twitter_Reply | 用户在Twitter上随时回复 |
| Twitter_Like | 将内容共享到的位置：转推 |
| Livefyre(_L) | 任何时候在应用程序中使用livefyre类似功能 |
| Livefyre(_N) | 任何时候用户都会像 |
| ShareOnPost | 随时，用户发布内容并使用“发布时共享”功能 |
| ShareButtonClick | 用户单击评论上的共享按钮时 |
| 共享Twitter | 单击“共享到Twitter”时 |
| ShareFacebook | 单击“共享到Facebook”时 |
| ShareURL | 选择/复制“共享到URL”文本区域时。 |
| 扩展回复 | 当用户单击+或展开链接以视图顶级帖子上的所有回复时 |
| 折叠回复 | 当用户单击 — 或折叠链接以视图顶级帖子上的所有回复时 |
| FlagClick | 用户随时打开标志模式 |
| FlagSpam | 当用户将内容标记为垃圾邮件时 |
| 旗标反对 | 当用户将内容标记为不同意 |
| FlagOffensive | 当用户将内容标记为冒犯 |
| FlagOffTopic | 当用户将内容标记为关闭主题时 |
| 标记取消 | 用户在提交标记时单击X或“取消” |
| FollowCollection | 每次对话后（“我对评论感兴趣”） |
| UnfollowCollection | 取消对话后 |
| 请求更多 | 任何时候用户在应用程序中加载更多内容（也需要高速） |
| ModalView | 用户单击以模式视图内容时 |
| TwitterRetweetClick | 将内容共享到的位置：转推 |
| PostButtonClick | 当用户点击帖子（“您在想什么？”）时 按钮 |
| 登录 | 任何用户登录时 |
| 注销 | 用户每次注销 |

以下是Livefyre提供的转换变量(eVar)列表。

## 转换变量 — eVar

| 事件 | 描述 |
|--- |--- |
| 网络ID | Livefyre中的网络ID/名称 |
| 应用程序 ID | 应用程序的URN |
| 上下文ID | Livefyre中的内容ID |
| 应用程序类型 | Livefyre应用程序类型。 选项: <br><ul><li>实时博客  </li><li> 功能卡</li><li>轮播</li><li>聊天 </li><li>注释</li><li>幻灯片</li><li>地图</li><li>马赛克</li><li>媒体墙</li><li>趋势</li><li>上传按钮</li></ul> |
| 内容类型 | Instagram、Twitter、Facebook、LiveFyre、YouTube等 |

## 更多信息 {#section_b3d_4yl_pdb}

有关本页讨论的主题的详细信息，请参阅：

* [报表包管](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)[理器DTM](https://docs.adobe.com/content/help/en/livefyre/using/apps/filmstrip/c-filmstrip-app.html)

* [规则](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
