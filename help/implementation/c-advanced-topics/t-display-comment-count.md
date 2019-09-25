---
description: 获取特定集合的帖子和评论计数以在索引页面上显示。
seo-description: 获取特定集合的帖子和评论计数以在索引页面上显示。
seo-title: 显示评论计数
solution: Experience Manager
title: 显示评论计数
uuid: 0f39b25e-11e0-4945-be71-55fb4798b6c7
translation-type: tm+mt
source-git-commit: c287e7a880f956f0444af746adee682571fe5a72

---


# 显示评论计数{#display-comment-count}

获取特定集合的帖子和评论计数以在索引页面上显示。

Livefyre允许您 `CommentCount.js` 获取站点上集合的内容计数。 尽管应用程序将显示当前集合的注释计数，但让这些计数在您的网站中协同工作可能会很有用。 如果您不将内容保留在数据库中（或者您的CMS数据库未与Livefyre同步），则此功能特别有用。

1. 加载JavaScript。

   要使用 `CommentCount.js`JavaScript文件，请首先将JavaScript文件嵌入到 `<head>` 要使用它的页面或模板的部分。

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. 绑定HTML元素。

   加载脚本后，它将尝试在页面上查找类名为的其他元素 `livefyre-commentcount`。 对于这些元素，脚本将查找和 `data-lf-site-id``data-lf-article-id` HTML属性，并使用这些属性从Livefyre获取内容并使用最新值更新每个元素。

   例如，将更新以下元素：

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE] {importance="high"}
   >
   >代 `CommentCount.js` 码检查数字值以随实际计数进行更新。 请务必在标记之间包含一个数字值。

   **示例1** （使用URL作为文章ID）:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **示例2** （将编号系统用作文章ID）:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. 配置选项。

   要进一步控制内容计数的替换方式，请调 `LF.CommentCount()` 用并传入包含配置选项的对象。 确保在DOM中所有需要替换的元素都包含之后调用函数。 调用此方法的最佳位置在页脚中，因此在加载DOM时，但在文档和窗口就绪事件之前会发生这种情况。

   我们允许以下配置选项：

* **** replacer:用于替换每个内容计数的文本的函数或正则表达式。

* **** 函数：用于替换每个元素。 函数的参数有：

   **** 元素：正在更新的HTML元素。
   **** 计数：此元素的内容计数。

* **** 正则表达式：用于确定元素文本的哪一部分应替换为计数。

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
