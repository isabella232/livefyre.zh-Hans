---
description: 了解如何使用“C#”语言生成Livefyre令牌。
seo-description: 了解如何使用“C#”语言生成Livefyre令牌。
seo-title: 创建Livefyre令牌“C#”
solution: Experience Manager
title: 创建Livefyre令牌“C#”
uuid: c5e05625-8550-4b51-9211-134600e20ec7
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 2%

---


# 创建Livefyre令牌C\# {#creating-livefyre-tokens-c}

了解如何使用 ``C#`` 语言生成 Livefyre 令牌。

您可以利用旧版文档和示例代码使用`C#.NET`编写方法来创建令牌。

要引用Livefyre的官方库，请将[Java库](https://github.com/Livefyre/livefyre-java-utils)用作`C#`开发人员的起点。

您还可以考虑使用命令行中的[Node.js库](https://github.com/Livefyre/livefyre-nodejs-utils)为自己生成引用令牌，并熟悉方法结构。

* [跳转至集合元令牌](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [跳转至身份验证令牌](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## 依赖项{#section_c15_fnh_xz}

* 您需要项目中的[JWT nuget包](https://www.nuget.org/packages/JWT)才能生成令牌。
* 此页上的代码示例使用[Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/)包。

## CollectionMeta令牌{#section_dzt_4mh_xz}

在页面上嵌入注释时，CollectionMeta令牌会传递到Livefyre，并为我们的系统提供新集合所需的元数据。 此外，您还将创建此数据的MD5 `checksum`,Livefyre将检查该数据以查看元数据是否已更改。 （例如，您的文章的标题或url已编辑）。

此令牌已与您的`Site Key`签名，该令牌由Livefyre的技术客户经理提供。

另请参阅：

* 正式集合元令牌文档
* [示例Gist](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. 构建包含集合元数据的词典。 我们只打算在此步骤中添加一些必要的字段，因为在添加articleId之前，我们希望创建此对象的校验和。

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

   * **标** *题必填*:集合的标题，通常是文章的标题。最大长度为255个字符。 不支持html实体。 请使用UTF-8对特殊字符进行编码。
   * **必** *需*:文章的规范url。评论共享和社交同步功能将使用此选项，并从“管理员”仪表板链接到您的文章。 如果在本地进行测试，请注意，Livefyre将不接受“localhost”作为域。
   * **标** *语可选*:要添加到Livefyre列表中的集合的以逗号分隔的标记仪表板。标记不能包含空格。 如果您希望在“管理员”仪表板中显示空间，请使用下划线。
   * **** *typeoptional*:一个字符串，指示要创建的集合类型。有效值为：

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`

      如果未指定，则默认情况下会创建LiveComments集合。


1. JSON对此词典进行编码，并生成其md5校验和。

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

1. 将&#x200B;**articleId**&#x200B;添加到词典。 **checksum**&#x200B;不进入collectionMeta令牌，但应作为convConfig js对象中的单独参数发送。

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **文** *章必需*:Livefyre站点中您的集合的唯一标识符。通常，在CMS中使用的唯一articleId。 （例如您的WordPress帖子ID）此值不应更改。 Livefyre通过siteId和articleId的组合来标识唯一集合。

1. 使用Livefyre提供给您的站点密钥，生成字典的已签名JWT令牌。 请注意，必须指定正确的哈希算法，因为默认情况下JWT包不使用HS256。

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## 用户身份验证令牌{#section_g1d_43h_xz}

用户身份验证令牌用于将用户登录Livefyre。 当用户登录您的站点时，该站点将生成一个用户身份验证令牌，该令牌将传递到页面上的Livefyre构件。 (有关身份验证过程的详细信息，请参阅远程用户档案。)

此令牌需要您的网络名称(network.fyre.co)，并使用您的网络密钥进行签名，该密钥由Livefyre的技术客户经理提供给您。

另请参阅：

* 正式身份验证令牌文档
* [示例Gist](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. 构建包含必要信息的词典。

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **域：** 网络的名称（由Livefyre提供）。例如mynetwork.fyre.co
   * **user_id：站** 点用户档案系统中用户的唯一用户ID。只能是字母数字字符(A-Z、a-z、0-9)。 如果您的系统用户ID包含无效字符，请考虑发送用户ID的md5哈希或base64编码版本的Livefyre。 （如果您这样做，请告知客户经理。）
   * **expires:** 令牌过期的日期（在Epoch时间中）。这应该与您站点上登录的会话时间匹配，以使Livefyre的登录状态与您站点的登录状态保持同步。
   * **display_name:** 用户在用户档案系统中的显示名称，应当显示在注释流中。

1. 使用Livefyre提供给您的网络密钥，生成字典的已签名JWT令牌。 请注意，必须指定正确的哈希算法，因为默认情况下JWT包不使用HS256。

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
