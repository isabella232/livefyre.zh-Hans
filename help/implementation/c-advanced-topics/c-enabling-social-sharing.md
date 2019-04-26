---
description: 设置允许用户将内容共享到各种社交网络的凭据。
seo-description: 设置允许用户将内容共享到各种社交网络的凭据。
seo-title: 启用社交共享
solution: Experience Manager
title: 启用社交共享
uuid: f584a0ae-46c7-48c1-aea4-36da9 f1 e259 b
translation-type: tm+mt
source-git-commit: d77b633b9892e3ea4aaec860317887f1fdf66830

---


# 启用社交共享 {#enabling-social-sharing}

设置允许用户将内容共享到各种社交网络的凭据。

要允许用户跨社交媒体站点共享内容，请实施Livefyre的社交共享功能，并创建OAuth系统以为这些站点提供适当的身份验证。借助此系统，Livefyre在用户选择通过社交媒体共享内容时代表用户行事。

>[!NOTE]
>
>不同提供商具有不同的OAuth要求。请咨询提供商以获取与其实施OAuth相关的信息。

## 必需的社交凭据 {#section_gff_cjm_b1b}

如果您使用自定义用户标识系统，则必须提供社交凭据，使用户能够从Livefyre应用程序共享到Twitter、Facebook或LinkedIn。

>[!NOTE]
>
>使用Janrain Engage的客户只需提供其参与域和参与API密钥。

使用Admin Console的“集成设置”面板输入或更新以下社交凭据。

### 必需凭据：

* **Facebook** Client ID客户端机密OAuth代理重定向
* **LinkedIn** API密钥API机密
* **Twitter** 访问令牌访问令牌机密API密钥API机密

## Twitter {#section_qp5_1yl_b1b}

Twitter凭据可从Twitter应用程序控制面板获取。要查找这些凭据，请执行以下操作：

* 打开 [Twitter的App Dev页面](https://dev.twitter.com/apps) 作为应用程序所有者，找到应用程序并单击标题。
* 向下滚动至“您的访问令牌”，然后从“Access token”和“Access token Secret”中获取值。”

您必须：

* 在Twitter应用程序中输入回调URL字段的值。虽然此字段可能是一个简单的占位符，但它不能留空。
* 将应用程序类型设置为具有 **读写****** 访问权限。
* 确认Twitter应用程序网站URL与Livefyre核心应用程序位于同一主机域上。

>[!NOTE]
>
>所有显示Twitter内容的应用程序都必须遵循其显示要求。有关更多信息，请参阅 [Twitter显示指南](https://dev.twitter.com/terms/display-requirements) 。

## LinkedIn {#section_lfz_zxl_b1b}

LinkedIn凭据可从LinkedIn应用程序API密钥的OAuth Keys部分中获取。

* 从LinkedIn的开发人员页面 [https://developer.linkedin.com/登录您的帐户](https://developer.linkedin.com/)。
* 将鼠标悬停在右上方的姓名上方，然后从下拉菜单中选择API密钥。
* 单击应用程序标题。
* 从OAuth Keys部分获取API密钥和机密密钥值

## Facebook {#section_zyb_gpl_b1b}

可从您的开发人员应用程序页面获取Facebook凭据。

* 打开 [Facebook的开发人员应用程序页面](https://developers.facebook.com/apps) 作为应用程序所有者，找到应用程序并单击标题。
* 获取App ID和App Secret的值。对于App Secret，您可能需要单击“显示”按钮以显示它。

共享到Facebook要求您设置重定向页面以获取Facebook请求并遵守 [Facebook所要求的域惯例](https://developers.facebook.com/docs/reference/dialogs/oauth/)。页面必须托管在您的域中，因此Facebook可以验证请求是否来自某个合法源。

### Facebook重定向

托管页面应包含以下代码：

### Ruby

这是一个使用Ruby和Rails进行Facebook OAuth重定向的示例。

```ruby
require "base64" 
  
class Controller < ActionController::Base 
   def base64url_decode(str) 
      str.gsub! '-_', '+/' 
      Base64.decode64(str.ljust(str.length+str.length%4, '=')) 
   end 
  
   def index 
      lfoauth = params[:lfoauth] 
      if not lfoauth 
         render :status => :forbidden, :text => 'Missing lfoauth.' 
      end 
  
      redirect = base64url_decode lfoauth 
  
      match = /^(http:\/\/|https:\/\/)?([^\/?]+)/i.match(redirect) 
      host = match[2] 
  
         if not host.include? 'fyre.co' 
      render :status => :forbidden, :text => 'Invalid host.' 
         end 
  
         sep = (redirect.include? '?') ? '&' : '?' 
      params.delete :lfoauth 
  
         rdir = redirect + sep + params.to_query 
      redirect_to rdir 
   end 
end
```

### Python

这是一个使用Python和Django进行Facebook OAuth重定向的示例。

```python
import base64, re 
from django.views.decorators.http import require_GET 
from django.http.response import HttpResponseRedirect, HttpResponseBadRequest 
  
def base64url_decode(st): 
    return base64.b64decode(re.sub("-_","+/", st).ljust(len(st)+len(st)%4, '=')) 
  
@require_GET 
def handle_lfoauth(request): 
    lfoauth = request.GET.get('lfoauth', None) 
    import pdb; pdb.set_trace() 
    if not lfoauth: 
        return HttpResponseBadRequest('Missing lfoauth.') 
     
    redirect = base64url_decode(lfoauth) 
     
    match = re.match(r"^(http:\/\/|https:\/\/)?([^\/?]+)", redirect, re.IGNORECASE) 
    host = match.group(2) 
     
    # validate the destination to secure this proxy 
    if not 'fyre.co' in host: 
        return HttpResponseBadRequest('Invalid host.') 
     
    # if params were included in the uri already, append with &, otherwise ? 
    sep = '&' if '?' in redirect else '?' 
     
    # remove lfoauth from query param 
    dict_ = request.GET.copy() 
    dict_.pop('lfoauth') 
  
    # attach remaining param to redirect 
    rdir = redirect + sep + dict_.urlencode() 
  
    # this does the actual redirection 
    return HttpResponseRedirect(rdir)
```

### NodeJS

这是使用NodeJS和Sail/Express执行Facebook OAuth重定向的一个示例。

```nodejs
/* 
 * 
 */ 
var S = require('string'), 
     querystring = require('querystring'); 
  
var base64UrlDecode = function(str) { 
     var temp = S(str.replace('-_', '+/')).padRight(str.length+(str.length%4), '=').s 
     return new Buffer(temp, 'base64').toString('utf8'); 
} 
  
module.exports = { 
  index: function(req, res) { 
     var lfoauth = req.param('lfoauth'); 
  
     if (typeof lfoauth === 'undefined') { 
        res.send(400, 'Missing lfoauth.'); 
     } 
  
     var redirect = base64UrlDecode(lfoauth); 
  
     var match = redirect.match(/^(http:\/\/|https:\/\/)?([^\/?]+)/i); 
     var host = match[2] 
  
     if (host.indexOf('fyre.co') <= -1) { 
        res.send(400, 'Invalid host.'); 
     } 
  
     var sep = redirect.indexOf('?') > -1 ? '&' : '?'; 
  
     delete req.query['lfoauth']; 
     var rdir = redirect + sep + querystring.stringify(req.query); 
  
     res.redirect(rdir); 
  }, 
  
  _config: {} 
};
```

### Java

这是一个使用Java和Spring控制器进行Facebook OAuth重定向的示例。

```java
/* 
 *  
 */ 
import java.util.Collection; 
import java.util.HashMap; 
import java.util.Map; 
import java.util.regex.Matcher; 
import java.util.regex.Pattern; 
  
import org.apache.commons.codec.binary.Base64; 
import org.apache.commons.lang.StringUtils; 
import org.jboss.resteasy.spi.BadRequestException; 
import org.springframework.stereotype.Controller; 
import org.springframework.web.bind.annotation.RequestMapping; 
import org.springframework.web.bind.annotation.RequestParam; 
import org.springframework.web.servlet.View; 
import org.springframework.web.servlet.view.RedirectView; 
  
@Controller 
public class RedirectController { 
    @RequestMapping("/fbredirect") 
    public View facebook(@RequestParam Map<string,object> allRequestParams) { 
        if (!allRequestParams.containsKey("lfoauth")) { 
            throw new BadRequestException("Missing lfoauth."); 
        } 
             
        String redirect = base64UrlDecode((String) allRequestParams.get("lfoauth")); 
  
        Pattern p = Pattern.compile("^(http:\\/\\/|https:\\/\\/)?([^\\/?]+)", Pattern.CASE_INSENSITIVE); 
        Matcher m = p.matcher(redirect); 
        if (!m.find() || !m.group(2).contains("fyre.co")) { 
            throw new BadRequestException("Invalid host."); 
        } 
         
        Map<string, object=""> params = new HashMap<string, object="">(allRequestParams); 
        params.remove("lfoauth"); 
        String rdir = redirect + (redirect.contains("?") ? '&' : '?') + mapToQueryString(params); 
         
        return new RedirectView(rdir); 
    } 
     
    private String base64UrlDecode(String str) { 
        return new String(Base64.decodeBase64(StringUtils.rightPad(str.replaceAll("-_", "+/"), str.length()+(str.length()%4), '='))); 
    } 
     
    private String mapToQueryString(Map<string, object=""> map) { 
        String queryparam = ""; 
        for (String key : map.keySet()) { 
            if (map.get(key) instanceof Collection) { 
                for (Object item : (Collection) map.get(key)) { 
                    queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, item.toString())); 
                } 
            } else { 
                queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, map.get(key).toString())); 
            } 
        } 
        return StringUtils.removeEnd(queryparam, "&"); 
    } 
}
```

### PHP

```php
<?php 
/* 
Purpose: Provide a landing page for the last step of successful oAuth 
         that is on the correct (Facebook approved) domain. 
  
Location: This file should be hosted on the same domain as your  
          Facebook App's "site url". 
  
Input Parameters:  
    - (GET) lfoauth: This should be a url-safe base64-encoded URL that  
      is the "real" final redirection URL. Livefyre sets this. 
  
      For testing purposes, this can be set to a url-safe base64-encoded  
      URL of your choosing, but the domain name must end in .fyre.co in  
      order to be considered valid. 
  
    - (GET) [all other parameters]: Any other parameters should simply  
      be passed thru on the redirection URL. If the decoded URL from "lfoauth"  
      includes querystring parameters, then the additional parameters included  
      with the initial request should be appended with "&..." 
  
Output: The response should indicate that the browser redirect (302) to the  
        "real" URL which is encoded in the "lfoauth" parameter. 
  
*/ 
  
function base64url_decode($data) { 
  return base64_decode(str_pad(strtr($data, '-_', '+/'), strlen($data) % 4, '=', STR_PAD_RIGHT)); 
} 
  
if (isset($_GET['lfoauth'])) { 
    // Warning: If implemented with non-PHP, b64 may fail because we have  
    // stripped padding (trailing ='s), to comply with Facebook parameters.   
    // The decode needs to be non-strict in this sense. 
  
    $rdir = base64url_decode($_GET['lfoauth']); 
  
    // validate the destination to secure this proxy 
    preg_match("/^(https?:\/\/)?([^\/?]+)/i", $rdir, $domain_only);    
    $host = $domain_only[2]; 
    if (!strstr($host,'fyre.co')) { 
        echo "Error - this redirection is not allowed! ".$host; 
        exit; 
    } 
  
    // if params were included in the uri already, append with &, otherwise ? 
    $sep = strstr($rdir,'?') ? '&' : '?'; 
  
    // don't include this in the params we add to the redirect url 
    unset($_GET['lfoauth']); 
  
    // assemble a new querystring from the remaining inbound GET params 
    $rdir = $rdir.$sep.http_build_query($_GET); 
  
    // this does the actual redirection, PHP's implementation is weird 
    header('Location: '.$rdir); 
} 
?>
```

## 配置“帖子给”提供者 {#section_rdk_dpl_b1b}

默认情况下，Livefyre核心应用程序中显示Facebook、LinkedIn和Twitter“帖子到”按钮。使用postToButtons参数配置嵌入Livefyre应用程序时将显示的提供者。

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` 是具有以下任意子集的数组：

* tw：Twitter
* fb：Facebook
* li：LinkedIn
