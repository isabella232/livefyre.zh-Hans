---
description: 可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript 的事件。
seo-description: 可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript 的事件。
seo-title: 对话应用程序的Javascript事件
solution: Experience Manager
title: 对话应用程序的Javascript事件
uuid: cce112b5-7c3a-4721-9854-fc8471f3d5d0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 对话应用程序的Javascript事件{#javascript-events-for-conversation-apps}

可用于为对话应用程序（例如，Comments、Chat、Live Blog、Reviews 和 Sidenotes）绑定 JavaScript 的事件。

## 对话应用程序和活动列表 {#section_y4j_x4m_ybb}

以下是可用于对话应用程序的活动的矩阵。 X表示该活动可用于应用程序，N/A表示该活动不适用于应用程序，而无标记表示该活动不适用于该应用程序：

### 对话应用程序活动

| 事件 | 注释 | 聊天 | Liveblog | 评论 | Sidesk | 投票 | 趋势 |
|---|---|---|---|---|---|---|---|
| 初始化 | X | X | X | X | X |  |  |
| 载入 | X | X | X | X |  |  |  |
| 查看 | X | X | X | X |  |  |  |
| 帖子 | X | X | X | X |  | 不适用 | 不适用 |
| 已发布 | X | X | X | X | X | 不适用 | 不适用 |
| Twitter 回复 | X | X | X | 不适用 | 不适用 | 不适用 | 不适用 |
| Twitter赞 | X | X | X | 不适用 | 不适用 | 不适用 | 不适用 |
| LF like | X | X | X | X | 不适用 | 不适用 | 不适用 |
| LF不同 | X | X | X | X | 不适用 | 不适用 | 不适用 |
| 在帖子中共享 | X | X |  | X | 不适用 | 不适用 | 不适用 |
| 共享按钮 | X | X | X | X |  | 不适用 | 不适用 |
| 共享Twitter | X | X | X | X | X | 不适用 | 不适用 |
| 分享Facebook | X | X | X | X | X | 不适用 | 不适用 |
| 共享URL | X | X | X | X |  | 不适用 | 不适用 |
| 扩展回复 | X | 不适用 | X | X | 不适用 | 不适用 | 不适用 |
| 折叠回复 | X | 不适用 | X | X | 不适用 | 不适用 | 不适用 |
| 标记按钮 | X | X | X | X | 不适用 | 不适用 | 不适用 |
| 标记 | X | X | X | X | X | 不适用 | 不适用 |
| 标记取消 | X | X | X | X | 不适用 | 不适用 | 不适用 |
| 关注 | X | 不适用 | X | X | 不适用 | 不适用 | 不适用 |
| 取消关注 | X | 不适用 | X | X | 不适用 | 不适用 | 不适用 |
| 请求更多 | X | X | X | X | 不适用 | 不适用 | 不适用 |
| ModalView |  | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 |
| Twitter转推 | X | X | X | 不适用 | 不适用 | 不适用 | 不适用 |
| 发布按钮单击 | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 |
| 已更新评论计数 | X | X | X | X | 不适用 | 不适用 | 不适用 |
| 用户已登录 |  |  |  |  |  | 不适用 | 不适用 |
| 用户已注销 |  |  |  |  |  | 不适用 | 不适用 |
| 推荐评论 |  | 不适用 |  |  | 不适用 | 不适用 | 不适用 |
| 评论无特色 |  | 不适用 |  |  | 不适用 | 不适用 | 不适用 |
| 评论投票 | 不适用 | 不适用 | 不适用 | X | X | 不适用 | 不适用 |
| 投票选择 | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 |  | 不适用 |
| 选定趋势项 | N/.A | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 |  |
| 网络ID |  |  |  |  |  |  |  |
| 应用程序 ID | X | X | X | X |  |  |  |
| 上下文ID | X | X | X | X |  |  |  |
| 应用程序类型 | X | X | X | X |  |  |  |
| 内容类型 | X | X | X | X |  |  |  |
| 发布到应用程序的日期 |  |  |  |  |  |  |  |
| 登录到最终用户应用程序 |  |  |  |  |  |  |  |

