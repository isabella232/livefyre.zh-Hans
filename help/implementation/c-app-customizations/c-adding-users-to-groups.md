---
description: 向帐户添加用户标记以将用户添加到组。
title: 将用户添加到组
exl-id: 6e799c77-e815-40c2-ae06-bbd076df9fe7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---

# 将用户添加到组{#adding-users-to-groups}

向帐户添加用户标记以将用户添加到组。

用户标签可以用于专有和企业用户档案系统，并可以通过多种方式添加到帐户：

* 通过Studio创建所有者和审核者将“审查方”用户标记分配给帐户。
* 创建用户组并通过Studio向用户添加用户，会自动将用户组名称的用户标签应用到选定用户。
* 用户标记也可以使用[添加用户标记HTTP](https://api.livefyre.com/docs#add-user-tag)调用或Ping for Pull直接应用于帐户。

>[!NOTE]
>
>API方法、HTTP添加用户标记调用和Ping for Pull方法都会通过其他方式覆盖之前分配给帐户的任何标记。 因此，请选择一种方法，并在整个过程中始终使用它。

## 从Studio {#section_qgq_nbw_xz}的“用户”页面将用户添加到“组”

* 单击&#x200B;**[!UICONTROL Add Group]**&#x200B;或任何用户名下的组标签以打开组菜单。
* 滚动浏览列表并查找要将用户添加到的组。 您可以在下拉列表顶部的&#x200B;**[!UICONTROL Search]**&#x200B;框中输入组名称。
* 单击应将用户添加到的组旁边的复选框，然后点击返回。

用户的用户档案将显示用户组的名称（如果用户仅在一个用户组中）或用户所属的用户组数。

## 使用添加用户标记调用{#section_kn3_gbw_xz}将用户添加到组

将用户的LFToken和选定标记名称与POST请求一起传递

例如：

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


有关详细信息，请参阅API参考> [添加用户标记](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post)。

## 使用Ping for Pull {#section_kyj_11w_xz}将用户添加到组

使用标记数组将用户分配给用户组。 （标记可能包含1-63个字母数字和下划线字符。）

例如：

```
"tags": ["moderator", "brand_advocate"],
```

## 使用远程用户档案{#section_uyn_scv_xz}将用户添加到组

向远程用户档案添加用户标记，该标记用于为特定用户在自定义用户档案系统和Livefyre之间同步用户数据。
