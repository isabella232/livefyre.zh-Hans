---
description: 安装Livefyre服务器端任务的库
seo-description: 安装Livefyre服务器端任务的库
seo-title: 安装
solution: Experience Manager
title: 安装
uuid: f60b4cc7-178f-4a16-ba75-f1 d0 d171 c52 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 安装{#installation}


## Java {#section_yd3_3zk_rz}

要安装Java库，请将此依赖关系添加到项目的OM：

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

Java库具有以下模块的依赖关系：

```
<dependency> 
   <groupId>com.sun.jersey</groupId> 
   <artifactId>jersey-client</artifactId> 
   <version>[1.18.1,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.code.gson</groupId> 
   <artifactId>gson</artifactId> 
   <version>[2.3,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.guava</groupId> 
   <artifactId>guava</artifactId> 
   <version>[18.0,)</version> 
</dependency> 
<dependency> 
   <groupId>org.apache.commons</groupId> 
   <artifactId>commons-lang3</artifactId> 
   <version>[3.0.1,)</version> 
</dependency> 
<dependency> 
   <groupId>org.bitbucket.b_c</groupId> 
   <artifactId>jose4j</artifactId> 
   <version>[0.4.1,)</version> 
</dependency> 
```

有关详细信息，请阅读Java文档或在GitHub上 [查看源](https://github.com/Livefyre/livefyre-java-utils)代码。

## NodeJS {#section_swj_pwq_rz}

要安装NodeJS库，请运行此行：

`$ npm install livefyre`

NodeJS库具有以下模块的依赖关系：

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

有关详细信息，请阅读NodeJS文档或在GitHub上 [查看源](https://github.com/Livefyre/livefyre-nodejs-utils)代码。

链接： [Restler](https://github.com/danwrong/restler)、 [Validator](https://www.npmjs.org/package/validator)、 [jsonwebten](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

要使用Composer安装PHP库，请将此组件添加到composer. json：

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

然后使用以下方法安装：

```
composer.phar install 
```

如果您 **不** 使用Composer，请使用以下方法获取最新版本的库：

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

要使用库，请将以下内容添加到PHP脚本：

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

PHP库具有以下模块的依赖关系：

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

有关详细信息，请阅读PHP文档或在GitHub上 [查看源](https://github.com/Livefyre/livefyre-php-utils)代码。

链接： [ext-json](https://php.net/manual/en/book.json.php)， [请求](https://github.com/rmccue/Requests/)， [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

要安装Python库，请运行此行：

`$ pip install livefyre`

Python库具有以下模块的依赖关系：

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

有关详细信息，请阅读Python文档或在GitHub上 [查看源](https://github.com/Livefyre/livefyre-python-utils)代码。

链接： [PyJWT](https://github.com/progrium/pyjwt)、 [Requests](https://github.com/kennethreitz/requests)、 [Python-Datetil](https://pypi.python.org/pypi/python-dateutil)、 [Enum34](https://pypi.python.org/pypi/enum34)、 [OrderEddt](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

要安装Ruby库，请将此行添加到应用程序的“gemfile”：

```
gem 'livefyre' 
```

或者自行安装：

`$ gem install livefyre`

Ruby库具有以下模块的依赖关系：

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

有关详细信息，请阅读Ruby文档或在GitHub上 [查看源](https://github.com/Livefyre/livefyre-ruby-utils)代码。

链接： [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)、 [REST Client](https://github.com/rest-client/rest-client/)、 [Addressable](https://github.com/sporkmonger/addressable)
