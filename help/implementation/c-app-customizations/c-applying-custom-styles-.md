---
description: 要为用户组自定义样式内容，必须首先向帐户添加一个用户标记，然后使用CSS设置内容样式。
seo-description: 要为用户组自定义样式内容，必须首先向帐户添加一个用户标记，然后使用CSS设置内容样式。
seo-title: 应用自定义样式
solution: Experience Manager
title: 应用自定义样式
uuid: 0556aa2f-4fcd-4bde-abb5-479ec682 f573
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 应用自定义样式{#applying-custom-styles}

要为用户组自定义样式内容，必须首先向帐户添加一个用户标记，然后使用CSS设置内容样式。

对于通过Studio添加的每个用户标签或Ting for Draw，Livefyre将创建两个CSS类，这两个CSS类都可用于设置用户组的内容样式。

将用户标记转换为CSS类时：

* Livefyre创建两类：fyre-author-tag-***< your_ group>***和fyre-tag-author-***< your_ group>***。两者都可用于设置内容样式。

* 标记中包含的任何空格都将转换为下划线。例如：“最喜欢的用户”将成为喜爱的_用户。
* 用户组名称中包含的Unicode字符将不会转换，并且将在类名称中显示为Unicode。例如：用户组“modérateur”将变为fyre-comment-author-tag-modér。

创建用户组后，使用Livefyre的CSS类为内容应用自定义样式。

## 为版主(和所有者)提供样式内容 {#section_vjv_2cv_xz}

* 使用CSS class. fyre-主持人。

   >[!NOTE]
   >
   >所有者，因为他们也是审核者，因此也将此类应用于流中的内容。

* 创建CSS规则以显示或样式组的徽章：

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## 用户组的样式内容 {#section_ghn_s1v_xz}

创建CSS规则以显示或样式组的徽章：

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

使用CSS类fyre-author-tag-***< your_ group>***或fyre-tag-author-***< your_ group>***为从与选定标记关联的帐户发布的每个项目设置字体和背景。

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

