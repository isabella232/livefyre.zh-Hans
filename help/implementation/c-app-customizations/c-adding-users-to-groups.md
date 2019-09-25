---
description: 向帐户添加用户标记以将用户添加到组。
seo-description: 向帐户添加用户标记以将用户添加到组。
seo-title: 将用户添加到用户组
solution: Experience Manager
title: 将用户添加到用户组
uuid: 3633f2df-8d60-4cdd-b9a2-3807218c74a0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Adding Users to Groups{#adding-users-to-groups}

向帐户添加用户标记以将用户添加到组。

用户标记可以用于专有和企业配置文件系统，并可以通过以下几种方式添加到帐户：

* 通过Studio创建所有者和审核者将“审查方”用户标记分配给帐户。
* 创建用户组并通过Studio向用户添加用户后，会自动将用户标记和用户组名称一起应用到选定用户。
* 用户标记也可以使用“添加用户标记HTTP”调 [用或“Ping for Pull”](https://api.livefyre.com/docs#add-user-tag) ，直接应用于帐户。

>[!NOTE]
>
>API方法、HTTP添加用户标记调用和Ping for Pull方法都将覆盖之前通过其他方式分配给帐户的所有标记。 因此，请选择一种方法，并在整个过程中一致地使用它。

## 从Studio的“用户”页面将用户添加到用户组 {#section_qgq_nbw_xz}

* 单击 **[!UICONTROL Add Group]** 或任何用户名下方的组标签以打开组菜单。
* 滚动浏览列表并查找要添加用户的组。 您可以在下拉列表顶部的 **[!UICONTROL Search]** 框中输入用户组名称。
* 单击应将用户添加到的用户组旁边的复选框，然后点击返回。

用户的配置文件将显示用户组的名称（如果用户仅在一个用户组中）或用户所属的用户组数。

## 使用“添加用户标记”调用将用户添加到用户组 {#section_kn3_gbw_xz}

将用户的LFToken和选定的标记名称与POST请求一起传递

例如：

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


有关详细信息，请参阅“API参考”&gt;“添 [加用户标记”](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post)。

## 使用Ping for Pull将用户添加到组 {#section_kyj_11w_xz}

使用标记数组将用户分配到用户组。 （标记可能包括1-63个字母数字和下划线字符。）

例如：

```
"tags": ["moderator", "brand_advocate"],
```

## 使用远程配置文件将用户添加到用户组 {#section_uyn_scv_xz}

向远程配置文件添加用户标记，用于为特定用户在自定义配置文件系统和Livefyre之间同步用户数据。
