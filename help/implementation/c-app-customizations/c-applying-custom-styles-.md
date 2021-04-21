---
description: 要为用户组自定义样式内容，您必须首先向帐户添加用户标记，然后使用CSS设置内容样式。
title: 应用自定样式
exl-id: 54692525-32ce-487a-b3c3-da1261b58da1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 应用自定义样式{#applying-custom-styles}

要为用户组自定义样式内容，您必须首先向帐户添加用户标记，然后使用CSS设置内容样式。

对于通过Studio或Ping for Pull添加的每个用户标签，Livefyre将创建两个CSS类，这两个类都可用于设置组内容的样式。

将用户标记转换为CSS类时：

* Livefyre创建两个类：fyre-author-tag-***&lt;your_group>****和fyre-tag-author-***&lt;your_group>*****。 两种方式均可用于设置内容的样式。

* 标记中包含的任何空格都将转换为下划线。 例如：“Favorite User”将变为favorite_user。
* 组名称中包含的Unicode字符将不进行转换，并在类名称中显示为Unicode。 例如：用户组“modérateur”将成为fyre-comment-author-tag-modérateur。

创建用户组后，使用Livefyre的CSS类为内容应用自定义样式。

## Style content for Moderators(and Owners){#section_vjv_2cv_xz}

* 使用CSS类.fyre-drocument。

   >[!NOTE]
   >
   >所有者也是版主，因此也会将此类应用于流中的内容。

* 创建CSS规则以显示或设置组徽章的样式：

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## 用户组{#section_ghn_s1v_xz}的样式内容

创建CSS规则以显示或设置组徽章的样式：

```
<span class="fyre-comment-author-tag fyre-comment-author-tag-writer fyre-comment-plus" data-fyre-author-tag="staff">Staff Writer</span>
```

```
.livechat-comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag, .comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag { 
    display: inline-block !important; 
    background: #603url('/etc/designs/site/images/comments-icon-staff.8db5be91.png?1438807177') no-repeat left center !important; 
    padding-right: 3px !important; 
    padding-left: 20px !important; 
    text-transform: uppercase !important; 
    font-weight: bold !important; 
    font-size: 11px !important; 
    border-radius: 0 !important; 
    color: #ffffff !important; 
}
```

使用CSS类fyre-author-tag-***&lt;your_group>***或fyre-tag-author-***&lt;your_group>****，为从与所选标记关联的帐户发布的每个项目设置字体和背景样式。

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```
