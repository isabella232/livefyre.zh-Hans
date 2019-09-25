---
description: 要为用户组自定义样式内容，必须首先向帐户添加用户标记，然后使用CSS设置内容样式。
seo-description: 要为用户组自定义样式内容，必须首先向帐户添加用户标记，然后使用CSS设置内容样式。
seo-title: 应用自定义样式
solution: Experience Manager
title: 应用自定义样式
uuid: 0556aa2f-4fcd-4bde-abb5-479ec682f573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 应用自定义样式{#applying-custom-styles}

要为用户组自定义样式内容，必须首先向帐户添加用户标记，然后使用CSS设置内容样式。

对于通过Studio或Ping for Pull添加的每个用户标签，Livefyre将创建两个CSS类，这两个类均可用于设置组内容的样式。

将用户标记转换为CSS类时：

* Livefyre创建两个类：fyre-author-tag-***&lt;your_group&gt;***和fyre-tag-author-***&lt;your_group&gt;****。 两种方法都可用于设置内容的样式。

* 标记中包含的所有空格将转换为下划线。 例如：“Favorite User”将变为favorite_user。
* 组名称中包含的Unicode字符将不会转换，并且在类名称中将显示为Unicode。 例如：用户组“modérateur”将成为fyre-comment-author-tag-modérateur。

创建用户组后，使用Livefyre的CSS类为内容应用自定义样式。

## 版主（和所有者）的样式内容 {#section_vjv_2cv_xz}

* 使用CSS类。fyre-droducator。

   >[!NOTE]
   >
   >所有者也是版主，因此也将此类应用于流中的内容。

* 创建CSS规则以显示组徽章或为组设计徽章样式：

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## 为用户组设置内容样式 {#section_ghn_s1v_xz}

创建CSS规则以显示组徽章或为组设计徽章样式：

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

使用CSS类fyre-author-tag-***&lt;your_group&gt;***或fyre-tag-author-***&lt;your_group&gt;****为从与所选标记关联的帐户发布的每个项目设置字体和背景样式。

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

