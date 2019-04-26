---
description: null
seo-description: null
seo-title: 使用亵渎过滤器
solution: Experience Manager
title: 使用亵渎过滤器
uuid: b0b1fbae-c88 c-403c-9b91-df6620675 f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 使用亵渎过滤器{#using-the-profanity-filter}

检查发布到Livefyre App中的所有内容以获得亵渎。如果在内容或用户的显示屏名称中找到了包含在亵渎列表中的词语，则将标记该内容“亵渎性”，允许您对其进行筛选，以便进行审核、规则、模型或应用程序内容中的常规搜索。

>[!NOTE]
>
>Studio管理员和管理者的内容不受“亵渎规则”检查的约束，主持人发布的内容不会被标记。

Livefyre提供默认的亵渎列表。您可以选择在网络级别应用此列表、提供自己的列表或使用这两个列表的集合。网络中的各个站点可能继承网络亵渎列表，或使用自定义列表以特定于站点。

要提供您自己的自定义亵渎列表作为网络默认列表，请将其发送给Livefyre客户经理。

## 启用亵渎过滤功能 {#section_yqc_qsk_f1b}

在网络和站点级别支持和配置亵渎性过滤器。禁用网络级别的亵渎过滤器，以自动禁用从网络继承的所有站点的亵渎性过滤器。

>[!NOTE]
>
>检查通过Livefyre传递的所有内容均表示亵渎。如果发现包含默认SAFE亵渎列表或自定义亵渎列表中包含的词语，则标记为“亵渎性”。”要将Livefyre设置为自动对这些项目执行操作，请转 **[!UICONTROL Enable Profanity Checking]** 至 **[!UICONTROL ON]**。

## 为网络启用亵渎过滤器 {#section_twd_ssk_f1b}

1. 从 **[!UICONTROL Network]** 网络下拉菜单中进行选择。
1. **[!UICONTROL Settings > Network Settings > Moderation]**转至。
1. 向下滚动至并 **[!UICONTROL Profanity List]**设置 **[!UICONTROL Enable Profanity Checking]** 为 **[!UICONTROL ON]**。

1. 使用 **[!UICONTROL Update Network Profanity List]** 该字段向列表中添加单词，或单击某个单词将其从列表中删除。

>[!NOTE]
>
>编辑网络级别的“亵渎列表”不会影响已经到位的站点级别列表。要确保网络所做的更改对站点进行了更改，请在 **[!UICONTROL Restore Network List]** 更改完成后为站点选择。

## 为站点启用亵渎过滤器 {#section_fld_wsk_f1b}

1. 从网络下拉菜单中选择站点。
1. **[!UICONTROL Settings > Site Settings > Moderation]**转至。
1. 向下滚动到并 **[!UICONTROL Profanity List]** 设置 **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**为。

1. 选择以下选项之一：

   * 要继承网络中的“亵渎列表”(不常见)，请设置 **[!UICONTROL Use Site Profanity List]** 为 **[!UICONTROL OFF]**。

   * 要专门编辑站点的亵渎列表，请设置 **[!UICONTROL Use Site Profanity List]** 为 **[!UICONTROL On]** 打开该字段，您可以在该 **[!UICONTROL Update Profanity List]** 字段中编辑该列表：

      * 要删除单词，请单击该单词。
      * 要添加单词，请在 **[!UICONTROL Add new word]** 框中键入单词并点击 **[!UICONTROL Return]**。

      * 要查看列表中是否包含单词，请将单词键入 **[!UICONTROL Test profanity filter]** 框中。
   * 要重新导入网络亵渎列表并将其应用到网站，请单击 **[!UICONTROL Restore Network List]**。
   * 要清除列表中的所有内容并从头开始，请单击 **[!UICONTROL Clear List]**。


## 处理包含亵渎性的内容 {#section_epy_dtk_f1b}

使用“亵渎列表”帮助筛选内容搜索以及为ModQ创建预审核规则。

要搜索包含亵渎性的内容，请转到 **[!UICONTROL Library > App Content]**并 **[!UICONTROL Filter by Flags]** 选中该 **[!UICONTROL Profanity]** 复选框。将显示已被所选网站或网络的“亵渎过滤器”捕获的所有内容。此列表将包括使用SearchSync和流提取到应用程序中的内容。

要创建预审核规则，请从Studio选择 **[!UICONTROL Settings > Network Settings > Moderation]**。启用亵渎过滤器后，将显示新规则，允许您标记或审核包含亵渎内容的内容。默认情况下，此规则自动支持 **[!UICONTROL Premoderate]** 可更改为 **[!UICONTROL Trash it]** 或 **[!UICONTROL Bozo it]**的亵渎内容。

>[!NOTE]
>
>如果一条内容受到多个规则类型(如SAFE和标记规则)的约束，则将应用更严格的内容。例如：如果您的审核规则表示要审核某段内容，但安全规则表示该内容是“废纸篓”，则该规则将被“废纸篓”。

## 查看和更新网络的亵渎列表 {#section_qdb_btk_f1b}

1. **[!UICONTROL Settings > Network Settings > Moderation]**转至。
1. 向下滚动到 **[!UICONTROL Profanity List]** 章节。
1. 设置 **[!UICONTROL Enable Profanity Checking]****[!UICONTROL On]** 为显示为网络启用的List(Livefyre默认值或上传的自定义列表)并对其进行编辑。您可以通过以下方式编辑列表：
   * 要删除单词，请单击该单词。
   * 要添加单词，请在 **[!UICONTROL Add new word]** 框中键入单词并点击 **[!UICONTROL Return]**。
   * 要查看列表中是否包含单词，请将单词键入 **[!UICONTROL Test profanity filter]** 框中。

>[!NOTE]
>
>只有Studio管理员和版主才能编辑“亵渎列表”。

