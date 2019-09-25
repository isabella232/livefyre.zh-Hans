---
description: 2018年1月18日版本的发行说明。
seo-description: 2018年1月18日版本的发行说明。
seo-title: 2018 年 1 月 18 日
solution: Experience Manager
title: 2018 年 1 月 18 日
uuid: 8141f431-c154-4c8f-bbcd-b7c712fe5f7d
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# January 18, 2018{#january}

2018年1月18日版本的发行说明。

## 生产版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 错误 | 应用程序 | 修复了在使用jpeg文件时，Avatar无法正确呈现的错误。 |
| 错误 | ModQ | 修复了S1客户允许按ModQ中的集合筛选的错误。 |
| 错误 | 流 | 修复了在语言过滤器设置为“无”时破坏流规则的错误。 |
| 错误 | 流 | 修复了阻止保存Youtube流规则的错误。 |
| 错误 | 流 | 修复了用户可能在流规则中创建格式错误的地理条目并保存这些条目（这会导致流失败）的错误。 现在，用户无法再保存格式错误的地理标记。 |
| 错误 | Studio | 修复了阻止某些用户登录Livefyre的问题。 |

## UAT版本

| **问题类型** | **组件** | **发行说明** |
|---|---|---|
| 错误 | 库 | 安全错误修复。 现在，所有身份验证调用都使用HTTPS协议而不是HTTP进行。 |
| 增强功能 | 智能标记 | 流内容现在由Adobe Sensei自动智能标记，因为它已保存到文件夹或发布到应用程序。 |
| 错误 | 流 | 修复了Instagram流规则无法识别日文字符的问题。 |
| 增强功能 | 流 | 客户现在可以使用逻辑运算符(ANY、ALL、NOT)在流中创建详细的智能标签过滤器，这些过滤器可以创建更准确的内容。 For example if I use the hashtag #himalyas I can select to show only images that include "snowy" "mountains". |
| 错误 | Studio | 修复了在名称中显示特殊字符为HTML的错误。 |

