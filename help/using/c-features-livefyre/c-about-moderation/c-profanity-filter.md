---
description: 'null'
seo-description: 'null'
seo-title: 使用配置文件过滤器
solution: Experience Manager
title: 使用配置文件过滤器
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 使用配置文件过滤器{#using-the-profanity-filter}

系统会检查发布到Livefyre应用程序的所有内容是否有漏洞。 如果在内容中或用户的显示名称中找到包含在配置文件列表中的单词，则该内容将标为“Profity”，这样您便可以过滤该单词，以便进行预审核、规则、ModQ或应用程序内容中的常规搜索。

>[!NOTE]
>
>Studio管理员和管理者的内容不受“配置规则”检查的约束，主持人发布的内容也不会被标记。

Livefyre提供默认配置列表。 您可以选择在网络级别应用此列表，提供您自己的列表，或使用两者的集合。 网络中的各个站点可能继承网络配置文件列表，或者使用自定义为特定于站点的列表。

要提供您自己的自定义配置列表作为网络默认值，请将其发送给您的Livefyre客户经理。

## 启用不良过滤 {#section_yqc_qsk_f1b}

在网络和站点级别启用和配置配置文件过滤器。 在网络级别禁用配置文件过滤器，以自动禁用从网络继承的所有站点的配置文件过滤器。

>[!NOTE]
>
>通过Livefyre传递的所有内容都会检查其是否有漏洞。 如果发现包含默认SAFE配置文件列表或自定义配置文件列表中包含的词语的内容，则会将其标记为“配置文件”。要设置Livefyre自动对这些项目执行操作，请转 **[!UICONTROL Enable Profanity Checking]** 到 **[!UICONTROL ON]**。

## 为网络启用配置过滤器 {#section_twd_ssk_f1b}

1. 从网 **[!UICONTROL Network]** 络下拉菜单中进行选择。
1. 转至 **[!UICONTROL Settings > Network Settings > Moderation]**.
1. 向下滚动到 **[!UICONTROL Profanity List]**，并设置 **[!UICONTROL Enable Profanity Checking]** 为 **[!UICONTROL ON]**。

1. 使用字 **[!UICONTROL Update Network Profanity List]** 段向列表中添加单词，或单击单词将其从列表中删除。

>[!NOTE]
>
>编辑网络级别的“权限列表”不会影响任何已有的站点级别列表。 要确保对站点进行网络更改，请在 **[!UICONTROL Restore Network List]** 进行更改后选择站点。

## 为站点启用配置文件过滤器 {#section_fld_wsk_f1b}

1. 从网络下拉菜单中选择站点。
1. 转至 **[!UICONTROL Settings > Site Settings > Moderation]**.
1. 向下滚动到 **[!UICONTROL Profanity List]** 并设置 **[!UICONTROL Enable Profanity Checking]** 为 **[!UICONTROL ON]**。

1. 选择以下选项之一：

   * 要从网络继承配置列表（这不常见），请设置 **[!UICONTROL Use Site Profanity List]** 为 **[!UICONTROL OFF]**。

   * 要专门编辑站点的配置文件列表，请设置 **[!UICONTROL Use Site Profanity List]** 为打 **[!UICONTROL On]** 开 **[!UICONTROL Update Profanity List]** 字段，您可以在该字段中编辑列表：

      * 要删除单词，请单击该单词。
      * 要添加单词，请在框中键入该单 **[!UICONTROL Add new word]** 词并点击 **[!UICONTROL Return]**。

      * 要查看列表中是否包含单词，请在框中键入该 **[!UICONTROL Test profanity filter]** 单词。
   * 要重新导入网络“配置列表”并将其应用到站点，请单击 **[!UICONTROL Restore Network List]**。
   * 要从列表中清除所有内容并从头开始，请单击 **[!UICONTROL Clear List]**。


## 使用包含亵渎的内容 {#section_epy_dtk_f1b}

使用“配置文件列表”帮助过滤内容搜索并为ModQ创建预审核规则。

要搜索包含不良内容的内容，请转 **[!UICONTROL Library > App Content]**&#x200B;到并 **[!UICONTROL Filter by Flags]** 选中此复 **[!UICONTROL Profanity]** 选框。 将显示由所选站点或网络的配置文件过滤器捕获的所有内容。 此列表将包括使用SocialSync和Streams提取到应用程序中的内容。

要创建预审核规则，请从Studio中选择 **[!UICONTROL Settings > Network Settings > Moderation]**。 启用配置文件过滤器后，将显示新规则，允许您标记或预审包含配置文件的内容。 默认情况下，此规则自动 **[!UICONTROL Premoderate]** 启用配置文件内容(可更改为 **[!UICONTROL Trash it]** 或 **[!UICONTROL Bozo it]**)。

>[!NOTE]
>
>如果一条内容受多种规则类型（如SAFE和Flag规则）的约束，则应用更严格。 例如：如果您的“预审核”规则要求预审核某条内容，但“安全规则”要求“废弃”它，则它将被“删除”。

## 查看和更新网络的配置文件列表 {#section_qdb_btk_f1b}

1. 转至 **[!UICONTROL Settings > Network Settings > Moderation]**.
1. 向下滚动到该 **[!UICONTROL Profanity List]** 部分。
1. 设置 **[!UICONTROL Enable Profanity Checking]** 为显 **[!UICONTROL On]** 示为网络启用的列表（默认为Livefyre，或上传的自定义列表）并编辑它。 您可以通过以下方式编辑列表：
   * 要删除单词，请单击该单词。
   * 要添加单词，请在框中键入该单 **[!UICONTROL Add new word]** 词并点击 **[!UICONTROL Return]**。
   * 要查看列表中是否包含单词，请在框中键入该 **[!UICONTROL Test profanity filter]** 单词。

>[!NOTE]
>
>只有Studio管理员和版主才能编辑配置文件列表。

