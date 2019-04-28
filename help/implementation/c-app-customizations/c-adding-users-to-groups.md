---
description: 向帐户添加用户标记以向用户组添加用户。
seo-description: 向帐户添加用户标记以向用户组添加用户。
seo-title: 将用户添加到用户组
solution: Experience Manager
title: 将用户添加到用户组
uuid: 3633f2df-8d60-4cdd-b9 a2-38007218c74 a0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 将用户添加到用户组{#adding-users-to-groups}

向帐户添加用户标记以向用户组添加用户。

可以为专有和企业配置文件系统实施用户标记，并通过几种方式添加到帐户：

* 通过Studio创建所有者和版主，可将“主持人的用户标记”分配给帐户。
* 创建用户组并通过Studio将用户添加到用户组，会自动将用户标记与选定用户的名称一起应用。
* 用户标记也可以使用 [添加用户标记HTTP](https://api.livefyre.com/docs#add-user-tag) 调用直接应用到帐户，或为拉动而推送。

>[!NOTE]
>
>两种API方法(HTTP添加用户标签调用和“用于提取方法的ping”方法)都将覆盖之前通过其他方法分配给帐户的任何标记。因此，请选择一种方法，并在整个过程中一致地使用它。

## 通过Studio中的用户页面将用户添加到用户组 {#section_qgq_nbw_xz}

* 单击 **[!UICONTROL Add Group]** 或用户名下方的组标签可打开用户组菜单。
* 滚动列表并找到要添加用户的用户组。您可以在下拉菜单顶部的 **[!UICONTROL Search]** 框中输入组名称。
* 单击要添加用户的用户组旁边的复选框，然后点击返回。

用户的配置文件将显示用户组的名称(如果用户仅在一组中)或用户所属用户组的数量。

## 使用添加用户标记调用将用户添加到用户组 {#section_kn3_gbw_xz}

使用POST请求通过用户的LFToken和选定的标记名称

例如：

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


有关详细信息，请参阅API参考&gt; [添加用户标记](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post)。

## 使用“为拉取”将用户添加到用户组 {#section_kyj_11w_xz}

使用标记数组将用户分配给用户组。(标记可能包括1-63字母数字和下划线字符。)

例如：

```
"tags": ["moderator", "brand_advocate"],
```

## 使用远程配置文件将用户添加到用户组 {#section_uyn_scv_xz}

向远程配置文件添加用户标记，用于在自定义配置文件系统和Livefyre之间为特定用户同步用户数据。
