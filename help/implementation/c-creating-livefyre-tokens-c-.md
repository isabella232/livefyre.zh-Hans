---
description: 了解如何使用'C#'语言生成Livefyre令牌。
seo-description: 了解如何使用'C#'语言生成Livefyre令牌。
seo-title: 创建Livefyre Tokens'C#'
solution: Experience Manager
title: 创建Livefyre Tokens'C#'
uuid: c5e05625-8550-4b51-9211-134600e20ec7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 创建Livefyre Tokens C\# {#creating-livefyre-tokens-c}

了解如何使用 ``C#`` 语言生成 Livefyre 令牌。

您可以利用旧版文档和示例代码编写 `C#.NET` 用于创建令牌的方法。

要引用Livefyre的官方库，请使用 [Java库](https://github.com/Livefyre/livefyre-java-utils) 作为 `C#` 开发人员的起点。

您还可以考虑使用命令行中 [的Node. js库](https://github.com/Livefyre/livefyre-nodejs-utils) 为自己生成参考令牌，并熟悉方法结构。

* [跳转到集合元令牌](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [跳转至Auth Token](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## 依赖关系 {#section_c15_fnh_xz}

* 要生成令牌，您需要在项目中有 [](https://www.nuget.org/packages/JWT) JWT noget包。
* 此页面上的代码示例使用 [NewTonSoft JSON](https://www.nuget.org/packages/newtonsoft.json/) 包。

## CollectionMeta令牌 {#section_dzt_4mh_xz}

在页面上嵌入评论时，CollectionMeta令牌会传递给Livefyre，并为我们的系统提供新集合的必要元数据。此外，您还将创建此数据的MD5 `checksum` ，Livefyre将检查元数据是否已更改。(例如，如果您的文章的标题或url已编辑)。

此令牌由您 `Site Key`的技术客户经理在Livefyre提供给您。

另请参阅:

* Official CollectionMeta令牌文档
* [Gist示例](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. 构建包含集合元数据的Dontonary。我们只会在此步骤中添加一些必要字段，我们希望在添加articleID之前创建此对象的校验和。

   ```
       // Site Key provided by Livefyre 
       string siteSecret = "ABCDE1234"; 
   
       var meta = new Dictionary<string, object>() { 
           {"title", "Kings win the Stanley Cup"}, 
           {"url", "https://www.website.com/kings-win-stanley-cup"}, 
           {"tags", "sports, hockey, stanley_cup"}, 
           {"type", "livecomments"} 
       };
   ```

   * **必填标题****：集合的标题，通常为文章的标题。最大长度为255个字符。不支持html实体。请使用UTF-8对特殊字符进行编码。
   * **url***需要*：文章的规范url。注释共享和社交同步功能以及从管理员仪表板链接到您的文章的链接。如果本地测试，请注意Livefyre不会接受“localhost”作为域。
   * **标记***可选*：您要添加到Livefyre仪表板中的集合的以逗号分隔的标记列表。标记不能包含空格。如果希望在管理员仪表板中显示空格，请使用下划线。
   * **类型***可选*：指示要创建的集合类型的字符串。有效值为：

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      如果未指定，则默认创建LiveComments集合。


1. JSON对此词典进行编码，并生成md校验和。

   ```
          var metaStr = JsonConvert.SerializeObject(meta); 
       byte[] hash; 
   
       using (var md5 = MD5.Create()) 
       { 
           hash = md5.ComputeHash(Encoding.UTF8.GetBytes(metaStr)); 
       } 
   
       StringBuilder sBuilder = new StringBuilder(); 
   
       // Loop through each byte of the hashed data  
       // and format each one as a hexadecimal string  
       for (int i = 0; i < hash.Length; i++) 
       { 
           sBuilder.Append(hash[i].ToString("x2")); 
       } 
   ```

1. 将 **articleID** 添加到词典。**校验和** 不进入collectionMeta令牌，但应作为seapConfig js对象中的seap速率参数发送。

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **articleID***必需*：Livefyre站点内的集合的唯一标识符。通常是CMS中使用的唯一ArticleID。(例如您的WordPress帖子ID)此值不应更改。Livefyre通过组合SiteID和ArticleID识别唯一集合。

1. 使用Livefyre提供给您的站点密钥，生成一个已签名的JWT令牌。请注意，您必须指定正确的哈希算法，因为JWT包默认不使用HS256。

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## 用户身份验证令牌 {#section_g1d_43h_xz}

用户身份验证令牌用于将用户签名到Livefyre中。当用户登录您的站点时，站点会生成一个将被传递到页面上Livefyre构件的User Auth Token。(有关身份验证过程的详细信息，请参阅远程配置文件。)

此令牌需要您的网络名称(网络. fyre. co)，并由您的网络密钥签名，由您的技术客户经理在Livefyre提供给您。

另请参阅:

* 官方Auth Token Docs
* [Gist示例](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. 构建包含必要信息的Dontonary。

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **域：** 网络的名称(由Livefyre提供)例如mynetwork. fyre. co
   * **user_ id：** 站点配置文件系统中用户的唯一用户ID。必须仅为字母数字字符(A-Z、a-z、0-9)。如果您的系统用户ID包含无效的字符集，请考虑发送用户id的md哈希哈希值或它的base64编码版本。(让您的客户经理知道您是否做到了这一点。)
   * **过期：** 令牌过期的日期(在Epoch时间)。此操作应与站点登录的会话时间匹配，以便Livefyre的登录状态保持与站点已登录状态同步。
   * **display_ name：** 用户在配置文件系统中的显示名称，因为它应该显示在注释流中。

1. 使用Livefyre提供给您的网络密钥，生成词典的已签名JWT令牌。请注意，您必须指定正确的哈希算法，因为JWT包默认不使用HS256。

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
