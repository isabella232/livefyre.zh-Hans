---
title: 使用“亵渎过滤器”
description: 使用“亵渎过滤器”
exl-id: 6ea7d913-f562-42a5-a6ea-241aa4e1089a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# 使用“亵渎过滤器”{#using-the-profanity-filter}

系统会检查发布到Livefyre应用程序的所有内容是否有不当。 如果在内容或用户的显示名称中找到包含在亵渎列表中的词，该内容将标为“亵渎”，允许您对预审、规则、ModQ或应用程序内容中的常规搜索进行筛选。

>[!NOTE]
>
>Studio管理员和管理者的内容不受“亵渎规则”检查的约束，主持人发布的内容将不会被标记。

Livefyre提供默认的亵渎列表。 您可以选择在网络级别应用此列表，提供您自己的列表，或使用两者的聚合。 网络中的各个站点可以继承网络“亵渎”列表，或者使用自定义为特定于站点的列表。

要提供您自己的自定义配置列表作为网络默认配置，请将其发送给您的Livefyre客户经理。

## 启用亵渎过滤{#section_yqc_qsk_f1b}

在网络和站点级别启用和配置配置文件筛选器。 在网络级别禁用配置文件过滤器，以自动禁用从网络继承的所有站点的配置文件过滤器。

>[!NOTE]
>
>通过Livefyre的所有内容都会被检查是否有漏洞。 如果找到包含默认SAFE亵渎列表或自定义“亵渎列表”中包含的词语的内容，则会将其标为“亵渎”。 要设置Livefyre自动对这些项目执行操作，请将&#x200B;**[!UICONTROL Enable Profanity Checking]**&#x200B;转换为&#x200B;**[!UICONTROL ON]**。

## 为网络{#section_twd_ssk_f1b}启用“不规范过滤器”

1. 从网络下拉菜单中选择&#x200B;**[!UICONTROL Network]**。
1. 转至 **[!UICONTROL Settings > Network Settings > Moderation]**.
1. 向下滚动到&#x200B;**[!UICONTROL Profanity List]**，将&#x200B;**[!UICONTROL Enable Profanity Checking]**&#x200B;设置为&#x200B;**[!UICONTROL ON]**。

1. 使用&#x200B;**[!UICONTROL Update Network Profanity List]**&#x200B;字段向列表添加单词，或单击某个单词将其从列表中删除。

>[!NOTE]
>
>编辑网络级别的“亵渎”列表不会影响任何已有的站点级列表。 要确保从网络对站点进行更改，请在更改后为站点选择&#x200B;**[!UICONTROL Restore Network List]**。

## 为站点{#section_fld_wsk_f1b}启用“不规范过滤器”

1. 从“网络”下拉菜单中选择站点。
1. 转至 **[!UICONTROL Settings > Site Settings > Moderation]**.
1. 向下滚动到&#x200B;**[!UICONTROL Profanity List]**&#x200B;并将&#x200B;**[!UICONTROL Enable Profanity Checking]**&#x200B;设置为&#x200B;**[!UICONTROL ON]**。

1. 选择以下选项之一：

   * 要从网络继承“亵渎列表”（这不常见），请将&#x200B;**[!UICONTROL Use Site Profanity List]**&#x200B;设置为&#x200B;**[!UICONTROL OFF]**。

   * 要专门编辑站点的“亵渎”列表，请将&#x200B;**[!UICONTROL Use Site Profanity List]**&#x200B;设置为&#x200B;**[!UICONTROL On]**&#x200B;以打开&#x200B;**[!UICONTROL Update Profanity List]**&#x200B;字段，在该字段中可以编辑该列表:

      * 要删除单词，请单击该单词。
      * 要添加单词，请在&#x200B;**[!UICONTROL Add new word]**&#x200B;框中键入该单词，然后点击&#x200B;**[!UICONTROL Return]**。

      * 要查看列表中是否包含某个词，请在&#x200B;**[!UICONTROL Test profanity filter]**&#x200B;框中键入该词。
   * 要重新导入网络“Profanity”列表并将其应用到站点，请单击&#x200B;**[!UICONTROL Restore Network List]**。
   * 要从头开始清除所有列表和开始，请单击&#x200B;**[!UICONTROL Clear List]**。


## 处理包含不雅内容{#section_epy_dtk_f1b}

使用“亵渎”列表帮助过滤内容搜索并为ModQ创建预审规则。

要搜索包含不良内容的内容，请转至&#x200B;**[!UICONTROL Library > App Content]**、**[!UICONTROL Filter by Flags]**&#x200B;并选中&#x200B;**[!UICONTROL Profanity]**&#x200B;复选框。 将显示由所选站点或网络的“配置文件过滤器”捕获的所有内容。 此列表将包括使用SocialSync和Streams拖入应用程序的内容。

要创建预审核规则，请从Studio中选择&#x200B;**[!UICONTROL Settings > Network Settings > Moderation]**。 启用“亵渎”过滤器后，将显示新规则，允许您标记或预审包含亵渎的内容。 默认情况下，此规则自动为profane内容启用&#x200B;**[!UICONTROL Premoderate]**，可将其更改为&#x200B;**[!UICONTROL Trash it]**&#x200B;或&#x200B;**[!UICONTROL Bozo it]**。

>[!NOTE]
>
>如果单个内容受多个规则类型（如SAFE和Flag规则）的约束，则应用更严格的规则。 例如：如果您的“预审核”规则指示预先审核某条内容，但“安全规则”指示删除该内容，则该内容将被“丢弃”。

## 视图并更新网络{#section_qdb_btk_f1b}的“不规范列表”

1. 转至 **[!UICONTROL Settings > Network Settings > Moderation]**.
1. 向下滚动到&#x200B;**[!UICONTROL Profanity List]**&#x200B;部分。
1. 将&#x200B;**[!UICONTROL Enable Profanity Checking]**&#x200B;设置为&#x200B;**[!UICONTROL On]**&#x200B;以显示为网络启用的列表(默认为Livefyre，或上传的自定义列表)并对其进行编辑。 您可以通过以下方式编辑列表:
   * 要删除单词，请单击该单词。
   * 要添加单词，请在&#x200B;**[!UICONTROL Add new word]**&#x200B;框中键入该单词，然后点击&#x200B;**[!UICONTROL Return]**。
   * 要查看列表中是否包含某个词，请在&#x200B;**[!UICONTROL Test profanity filter]**&#x200B;框中键入该词。

>[!NOTE]
>
>只有Studio管理员和版主才能编辑配置文件列表。
