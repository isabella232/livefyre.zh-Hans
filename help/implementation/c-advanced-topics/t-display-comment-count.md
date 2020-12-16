---
description: 获取特定集合的帖子和评论计数以显示在您的索引页面上。
seo-description: 获取特定集合的帖子和评论计数以显示在您的索引页面上。
seo-title: 显示注释计数
solution: Experience Manager
title: 显示注释计数
uuid: 0f39b25e-11e0-4945-be71-55fb4798b6c7
translation-type: tm+mt
source-git-commit: c2594f919f153d1230b3dc0370f31d64cb698146
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# 显示注释计数{#display-comment-count}

获取特定集合的帖子和评论计数以显示在您的索引页面上。

Livefyre的`CommentCount.js`允许您在站点上获取集合的内容计数。 虽然应用程序将显示当前集合的注释计数，但让这些计数在您的网站中协同使用可能会很有用。 如果您不将内容保留在数据库中（或CMS数据库未与Livefyre同步），则此功能特别有用。

1. 加载JavaScript。

   要使用`CommentCount.js`，请首先将JavaScript文件嵌入要使用它的页面或模板的`<head>`部分。

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. 绑定HTML元素。

   加载脚本后，它将尝试在类名为`livefyre-commentcount`的页面上查找其他元素。 对于这些元素中的每个元素，脚本将查找`data-lf-site-id`和`data-lf-article-id` HTML属性，并使用这些属性从Livefyre获取内容并使用最新值更新每个元素。

   例如，将更新以下元素：

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >`CommentCount.js`代码检查是否有值以使用实际计数进行更新。 请确保在标记之间包含一个数值。

   **示例** 1（将URL用作文章ID）:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **示例** 2（使用编号系统作为文章ID）:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. 配置选项。

   要进一步控制如何替换内容计数，请调用`LF.CommentCount()`并传入包含配置选项的对象。 确保在DOM中所有需要替换的元素都出现后调用函数。 调用此方法的最佳位置在页脚中，因此加载DOM时会发生这种情况，但在文档和窗口就绪事件之前。

   我们允许以下配置选项：

* **replacer：用** 于替换每个内容计数的文本的函数或正则表达式。

* **函数：** 用于对每个元素进行替换。函数的参数有：

   **元素** ：要更新的HTML元素。
   **计数：** 此元素的内容计数。

* **正则表** 达式：用于确定应由计数替换元素文本的哪个部分。

   **示例**：

   ```
      <script type="text/javascript"> LF.CommentCount({ 
        replacer: function(element, count) { 
            element.innerHTML = count +' Comment'+ (count === 1 ? '' : 's'); 
        } 
    }); 
   </script>
   ```

   >[!NOTE]
   >
   >使用替换器可自定义或国际化评论计数消息。
