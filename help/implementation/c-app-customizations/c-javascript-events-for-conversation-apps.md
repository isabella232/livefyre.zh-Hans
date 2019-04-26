---
description: 可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript
  的事件。
seo-description: 可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript
  的事件。
seo-title: 对话应用程序的Javascript事件
solution: Experience Manager
title: 对话应用程序的Javascript事件
uuid: cce112b5-7c3a-4721-9854-fc8471 f3 d5 d0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 对话应用程序的Javascript事件{#javascript-events-for-conversation-apps}

可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript 的事件。

## 对话应用程序和活动矩阵 {#section_y4j_x4m_ybb}

以下是用于对话应用程序的事件矩阵。X表示该活动可用于应用程序，N/A指示该活动不适用于应用程序，而不表示该活动不适用于该应用程序：

### 对话应用程序事件

| 事件 | 注释 | 聊天 | LiveBlog | 评论 | Siten表示 | 投票 | 趋势趋势 |
|---|---|---|---|---|---|---|---|
| Init | X | X | X | X | X |  |  |
| Load | X | X | X | X |  |  |  |
| View | X | X | X | X |  |  |  |
| Post | X | X | X | X |  | N/A | N/A |
| 已发布 | X | X | X | X | X | N/A | N/A |
| Twitter回复 | X | X | X | N/A | N/A | N/A | N/A |
| Twitter称赞 | X | X | X | N/A | N/A | N/A | N/A |
| LF等 | X | X | X | X | N/A | N/A | N/A |
| LF与 | X | X | X | X | N/A | N/A | N/A |
| 在帖子时共享 | X | X |  | X | N/A | N/A | N/A |
| 共享按钮 | X | X | X | X |  | N/A | N/A |
| 共享Twitter | X | X | X | X | X | N/A | N/A |
| 共享Facebook | X | X | X | X | X | N/A | N/A |
| 共享URL | X | X | X | X |  | N/A | N/A |
| ExpandReadies | X | N/A | X | X | N/A | N/A | N/A |
| 折叠回复 | X | N/A | X | X | N/A | N/A | N/A |
| 旗标按钮 | X | X | X | X | N/A | N/A | N/A |
| 旗标 | X | X | X | X | X | N/A | N/A |
| 标记取消 | X | X | X | X | N/A | N/A | N/A |
| 关注 | X | N/A | X | X | N/A | N/A | N/A |
| 未遵循 | X | N/A | X | X | N/A | N/A | N/A |
| 请求更多 | X | X | X | X | N/A | N/A | N/A |
| ModalView |  | N/A | N/A | N/A | N/A | N/A | N/A |
| Twitter Twitter | X | X | X | N/A | N/A | N/A | N/A |
| 帖子按钮单击 | N/A | N/A | N/A | N/A | N/A | N/A | N/A |
| 评论计数已更新 | X | X | X | X | N/A | N/A | N/A |
| 用户登录 |  |  |  |  |  | N/A | N/A |
| 用户已注销 |  |  |  |  |  | N/A | N/A |
| 注释功能 |  | N/A |  |  | N/A | N/A | N/A |
| 注释未特色 |  | N/A |  |  | N/A | N/A | N/A |
| 投票投票 | N/A | N/A | N/A | X | X | N/A | N/A |
| 投票选择 | N/A | N/A | N/A | N/A | N/A |  | N/A |
| 选择的趋势项目 | N/. A | N/A | N/A | N/A | N/A | N/A |  |
| 网络ID |  |  |  |  |  |  |  |
| App ID | X | X | X | X |  |  |  |
| 上下文ID | X | X | X | X |  |  |  |
| 应用程序类型 | X | X | X | X |  |  |  |
| 内容类型 | X | X | X | X |  |  |  |
| 发布到应用程序的日期 |  |  |  |  |  |  |  |
| 登录到最终用户应用程序 |  |  |  |  |  |  |  |

