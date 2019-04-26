---
description: 获取某些集合的帖子和注释计数，以显示在索引页面上。
seo-description: 获取某些集合的帖子和注释计数，以显示在索引页面上。
seo-title: 显示评论计数
solution: Experience Manager
title: 显示评论计数
uuid: 0f39b25e-11e0-4945bb71-55fb4798b6c7
translation-type: tm+mt
source-git-commit: c287e7a880f956f0444af746adee682571fe5a72

---


# 显示评论计数{#display-comment-count}

获取某些集合的帖子和注释计数，以显示在索引页面上。

Livefyre允许 `CommentCount.js` 您获取网站上集合的内容计数。尽管应用程序将显示当前集合的评论计数，但在您的网站上汇总这些计数可能会很有用。如果您不保留数据库中的内容(或者您的CMS数据库未与Livefyre同步)，则此功能特别有用。

1. 加载JavaScript。

   要使用 `CommentCount.js`，首先将JavaScript文件嵌入到要使用它的页面或模板 `<head>` 部分中。

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. 绑定HTML元素。

   加载脚本后，它将尝试在页面上查找具有类名称的其他元素 `livefyre-commentcount`。对于每个元素，脚本将查找 `data-lf-site-id``data-lf-article-id` 和HTML属性，并使用这些属性从Livefyre中提取内容，并使用最新值更新每个元素。

   例如，将更新以下元素：

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE] {重要性=“high”}
   >
   >`CommentCount.js` 代码检查是否有一个数字值以实际计数进行更新。请确保在标记之间包含一个数字值。

   **示例1** (使用URL作为文章ID)：

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **示例2** (使用编号系统作为文章ID)：

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. 配置选项。

   要更多地控制内容计数的替换方式，请调用并 `LF.CommentCount()` 传入包含配置选项的对象。在DOM中需要替换所有元素之后，务必调用函数。调用此方法的最佳位置是footer，因此在DOM加载时，但在文档和窗口就绪事件之前发生。

   我们允许以下配置选项：

* **替换程序：** 函数或正则表达式用于替换每个内容计数的文本。

* **function：** 用于替换每个元素。该函数的参数有：

   **元素：** 正在更新的HTML元素。
   **count：** 此元素的内容计数。

* **regex：** 用于确定元素文本的哪部分应由计数替换。

   **示例**:

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
   >使用替换程序对注释计数消息进行自定义或国际化。
