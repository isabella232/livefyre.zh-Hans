---
product: livefyre
audience: end-user
user-guide-title: Livefyre实施指南
translation-type: tm+mt
source-git-commit: 3664bc1c51d2b372c358385127a1ca9c2f0cfef8
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 4%

---


# Livefyre实施指南 {#implementation}

+ [Livefyre实施指南](home.md)
+ 快速入门 {#getting-started}
   + [Livefyre集成入门](c-getting-started/c-getting-started.md)
   + 实施流程 {#implementation-process}
      + [实施流程](c-getting-started/c-implementation-process/c-implementation-process.md)
      + [应用程序集成类型](c-getting-started/c-implementation-process/c-app-integration-types.md)
      + [应用程序实施](c-getting-started/designer-app-implementation.md)
      + [通过第三方集成实施Livefyre](c-app-integrations/implement-livefyre-3rd-party.md)
      + [架构](c-getting-started/c-implementation-process/c-architecture.md)
      + [嵌入应用程序](c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)
      + [使用Livefyre.js将身份验证添加到应用程序](c-getting-started/c-implementation-process/c-add-authetication-to-an-app-using-livefyre.js.md)
      + [构建服务器端令牌](c-getting-started/c-implementation-process/c-build-server-side-tokens.md)
      + [集合元令牌](c-getting-started/c-implementation-process/c-collectionmeta-tokent.md)
      + [用户身份验证令牌](c-getting-started/c-implementation-process/c-user-auth-token.md)
      + [使用CollectionMeta令牌创建集合](t-create-a-collectionmeta-token.md)
      + [创建校验和](c-creating-a-checksum.md)
+ 身份集成 {#identity-integration}
   + [身份集成](t-about-identity-integration/t-about-identity-integration.md)
   + [身份验证包](t-about-identity-integration/c-authorization-package.md)
   + [AuthDelegate对象](t-about-identity-integration/c-building-an-auth-delegate.md)
   + [将用户权限发布到外部系统（可选）](t-about-identity-integration/c-posting-user-permissions-to-external-systems.md)
   + 实施SSO {#implementing-sso}
      + [实施SSO](t-about-identity-integration/c-implementing-sso/c-implementing-sso.md)
      + [调试身份验证委托](t-about-identity-integration/c-implementing-sso/c-debugging-auth.md)
   + 与Livefyre同步 {#sync-ping-for-pull}
      + [使用Ping for Pull与Livefyre同步](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)
      + [构建拉取端点](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-pull-endpoint.md)
      + [使用Studio注册端点](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-register-the-endpoint-with-studio.md)
      + [构建Ping](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-ping.md)
      + [拉式请求结构](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-pull-request-structure.md)
      + [构建Ping以进行拉式响应](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-build-the-ping-for-pull-response.md)
+ Livefyre Identity {#livefyre-identity}
   + [Livefyre Identity](c-livefyre-identity-comp/c-livefyre-identity-comp.md)
   + [启用Livefyre标识](c-livefyre-identity-comp/t-enable-livefyre-identity.md)
   + 将社交应用程序与Livefyre Identity结合使用 {#use-social-apps-with-livefyre-identity}
      + [创建社交应用程序](c-livefyre-identity-comp/t-create-your-social-apps.md)
      + [创建用于Livefyre Identity的Facebook应用程序](c-livefyre-identity-comp/t-create-a-facebook-app-for-use-with-livefyre-identity.md)
      + [创建用于Livefyre Identity的Twitter应用程序](c-livefyre-identity-comp/t-create-a-twitter-app-for-use-with-livefyre-identity.md)
      + [创建Yahoo! 与Livefyre Identity一起使用的应用程序](c-livefyre-identity-comp/t-create-a-yahoo-app-for-use-with-livefyre-identity.md)
      + [创建用于Livefyre Identity的Microsoft Live Identity应用程序](c-livefyre-identity-comp/t-create-a-microsoft-live-id-app-for-use-with-livefyre-identity.md)
      + [创建用于Livefyre Identity的LinkedIn应用程序](c-livefyre-identity-comp/t-create-a-linkedin-app-for-use-with-livefyre-identity.md)
      + [创建用于Livefyre Identity的GitHub Identity应用程序](c-livefyre-identity-comp/c-create-a-github-identity.md)
      + [使用Studio将您的社交应用程序连接到您的Livefyre实施](c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)
   + [将Livefyre.js添加到页面](c-livefyre-identity-comp/t-add-livefyre.js-to-the-page.md)
   + [初始化Livefyre标识](c-livefyre-identity-comp/t-initialize-livefyre-identity.md)
   + [Livefyre Identity的电子邮件](c-livefyre-identity-comp/c-emails-for-livefyre-identity.md)
   + [Janrain捕获／底板](c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)
   + 安装 {#installation}
      + [安装库](c-installing-libraries/c-installing-libraries.md)
      + [类和方法](c-installing-libraries/c-methods-livefyre.md)
      + [网络方法](c-installing-libraries/c-network-methods.md)
      + [setSSL网络方法](c-installing-libraries/r-setssl-method.md)
      + [buildLivefyreToken网络方法](c-installing-libraries/r-buildlivefyretoken-method.md)
      + [buildUserAuthToken网络方法](c-installing-libraries/r-builduserauthtoken-method.md)
      + [validateLivefyreToken网络方法](c-installing-libraries/c-validatelivefyretoken-network-method.md)
      + [setUserSyncUrl网络方法](c-installing-libraries/r-setusersyncurl-method.md)
      + [sync用户网络方法](c-installing-libraries/r-syncuser-method.md)
      + [getUrn网络方法](c-installing-libraries/r-geturn-method.md)
      + [getUrnForUser Network方法](c-installing-libraries/r-geturnforuser-method.md)
      + [getNetworkName网络方法](c-installing-libraries/r-getnetworkname-method.md)
      + [getSite网络方法](c-installing-libraries/r-getsite-method.md)
      + [网络类方法](c-installing-libraries/c-network-class-methods.md)
      + [集合类方法](c-installing-libraries/c-collection-methods.md)
      + [createOrUpdate收集方法](c-installing-libraries/r-createorupdate-collection-method.md)
      + [buildCollectionMetaToken集合方法](c-installing-libraries/r-buildcollectionmetatoken-collection-method.md)
      + [buildChecksum收集方法](c-installing-libraries/r-buildchecksum-collection-method.md)
      + [getCollectionContent Collection方法](c-installing-libraries/t-getcollectioncontent-collection-method.md)
      + [getUrn收集方法](c-installing-libraries/r-geturn-collection-method.md)
      + [站点类方法](c-installing-libraries/c-site-methods.md)
      + [buildBlogCollection站点方法](c-installing-libraries/r-buildblogcollection-site-method.md)
      + [buildChatCollection站点方法](c-installing-libraries/r-buildchatcollection-site-method.md)
      + [buildCommentsCollection站点方法](c-installing-libraries/r-buildcommentscollection-site-method.md)
      + [buildCountingCollection站点方法](c-installing-libraries/r-buildcountingcollection-site-method.md)
      + [buildRatingsCollection站点方法](c-installing-libraries/r-buildratingscollection-site-method.md)
      + [buildReviewsCollection站点方法](c-installing-libraries/r-buildreviewscollection-site-method.md)
      + [buildSitenotesCollection站点方法](c-installing-libraries/r-buildsitenotescollection-site-method.md)
      + [buildCollection站点方法](c-installing-libraries/r-buildcollection-site-method.md)
      + [getUrn站点方法](c-installing-libraries/r-geturn-site-method.md)
      + [示例](c-installing-libraries/c-libraries-examples.md)
   + Mobile SDK {#mobile-sdks}
      + [Mobile SDK](c-mobile-sdks/c-mobile-sdks.md)
      + [Livefyre iOS SDK](c-mobile-sdks/c-livefyre-ios-sdk.md)
      + [Android SDK](c-mobile-sdks/c-android-sdk.md)
+ [Livefyre.js](c-livefyre.js.md)
+ [创建Livefyre令牌C#](c-creating-livefyre-tokens-c-.md)
+ 应用程序集成 {#app-integrations}
   + [聊天](c-app-integrations/c-app-integratios-chat.md)
   + 注释 {#comments}
      + [评论](c-app-integrations/c-comments-integration/c-comments-integration.md)
   + [实时博客](c-app-integrations/c-live-blog-integration.md)
   + [评论](c-app-integrations/c-reviews-integration.md)
   + Sidesk {#sidenotes}
      + [Sisers集成](c-app-integrations/c-sidenotes-integration/r-sidenotes-integration.md)
      + [向页面添加指示符](c-app-integrations/c-sidenotes-integration/r-adding-sidenotes-to-a-page.md)
      + [Siestors应用程序事件](c-app-integrations/c-sidenotes-integration/r-app-events.md)
      + [指示配置选项](c-app-integrations/c-sidenotes-integration/r-configuration-options.md)
      + [表示自定义样式](c-app-integrations/c-sidenotes-integration/r-custom-styles.md)
      + [Sisers自定义字符串](c-app-integrations/c-sidenotes-integration/r-custom-strings.md)
      + [Sides Implementation](c-app-integrations/c-sidenotes-integration/r-sidenotes-implementation.md)
      + [updateAnchors方法](c-app-integrations/c-sidenotes-integration/update-anchors-method.md)
   + [地图](c-app-integrations/c-map-integration.md)
   + [媒体墙](c-app-integrations/c-media-wall-integration.md)
   + [趋势](c-app-integrations/c-trending-integration.md)
+ 应用程序自定义 {#app-customizations}
   + [应用程序自定义](c-app-customizations/c-app-customizations.md)
   + [更改显示选项](c-app-customizations/c-change-display-options.md)
   + [CSS类](c-app-customizations/c-css-classes.md)
   + [Storify CSS类](c-app-customizations/c-storify-css-classes.md)
   + [翻译集](c-app-customizations/c-translation-sets.md)
   + [移动Livefyre徽标](c-app-customizations/c-move-the-livefyre-logo.md)
   + [限制媒体](c-app-customizations/c-restrict-media.md)
   + [隐藏应用程序元素](c-app-customizations/c-hide-app-elements.md)
   + [更改 @mention 图标](c-app-customizations/c-change-mention-icon.md)
   + [突出显示内容](c-app-customizations/c-highlight-content.md)
   + [自定义日期和时间戳](c-app-customizations/c-date-time-stamp.md)
   + 功能内容 {#feature-content}
      + [功能内容](c-app-customizations/t-feature-content.md)
      + [在Studio中启用特色内容](c-app-customizations/t-enable-featuring-content-in-studio.md)
      + [从应用程序中选择要实现功能的内容](c-app-customizations/t-select-content-to-feature.md)
      + [从Studio中选择要显示的内容](c-app-customizations/t-select-content-to-feature-from-studio.md)
      + [使用CSS设计特色内容的样式](c-app-customizations/c-use-css-to-style-featured-content.md)
      + [功能API](c-app-customizations/c-feature-apis.md)
   + [使用AuthDelegate将Janrain连接到Livefyre](c-app-customizations/c-connecting-janrain-to-livefyre-using-authdelegate.md)
   + [使用特色API汇总特色内容](c-app-customizations/c-aggregated-featured-content-using-the-featured-apis.md)
   + 样式内容 {#style-content}
      + [样式用户组内容](c-app-customizations/c-style-user-group-content.md)
      + [将用户添加到组](c-app-customizations/c-adding-users-to-groups.md)
   + 应用自定义样式 {#apply-custom-styles}
      + [应用自定义样式](c-app-customizations/c-applying-custom-styles-.md)
      + [添加自定义按钮](c-app-customizations/t-add-custom-buttons.md)
   + Javascript事件 {#javascript-events}
      + [JavaScript事件定义和示例](c-app-customizations/c-javascript-events.md)
      + [可视化应用程序的Javascript事件](c-app-customizations/c-javascript-events-for-visualization-apps.md)
      + [媒体墙的Javascript事件](c-app-customizations/c-javascript-events-media-wall.md)
      + [对话应用程序的Javascript事件](c-app-customizations/c-javascript-events-for-conversation-apps.md)
   + [嵌入注释应用程序](c-app-customizations/c-embed-a-comments-app.md)
   + [推荐跟踪](c-app-customizations/c-referral-tracking.md)
   + [设备和浏览器支持](c-app-customizations/c-device-and-browser-support.md)
   + [Twitter显示要求](c-app-customizations/c-twitter-display-requirements.md)
+ [压力测试策略](c-stress-test-policy.md)
+ Analytics {#analytics}
   + [Analytics](livefyre-analytics/livefyre-analytics.md)
   + [将Livefyre与Adobe Analytics和Dynamic Tag Manager(DTM)结合使用](livefyre-analytics/c-use-livefyre-with-adobe-analytics.md)
   + [将Livefyre与其他分析工具结合使用](livefyre-analytics/c-livefyre-analytics.md)
   + [Livefyre Analytics事件](livefyre-analytics/c-livefyre-analytics-events.md)
+ [将Livefyre与AEM集成](c-livefyre-aem-integration.md)
+ 高级主题 {#advanced-topics}
   + [显示注释计数](c-advanced-topics/t-display-comment-count.md)
   + [启用社交共享](c-advanced-topics/c-enabling-social-sharing.md)
   + [活动流](c-advanced-topics/c-activity-stream.md)
   + [引导HTML](c-advanced-topics/c-bootstrap-html.md)
   + [更改集合](c-advanced-topics/c-change-collection.md)
   + [多个集合](c-advanced-topics/c-multiple-collections.md)
   + [切换核心应用程序类型](c-advanced-topics/c-switch-core-app-types.md)
   + [社交计数器](c-advanced-topics/c-social-counter.md)
   + [将Bootsrap和Stream API与Livefyre应用程序结合使用](c-advanced-topics/bootstrap-stream-api.md)
