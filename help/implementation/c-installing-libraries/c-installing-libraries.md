---
description: 为Livefyre服务器端任务安装库
title: 安装
exl-id: d74f85be-14c0-4f6d-8f16-b688282c0eb0
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---

# 安装{#installation}


## Java {#section_yd3_3zk_rz}

要安装Java库，请将此依赖项添加到项目的POM中：

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

Java库依赖于以下模块：

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

有关更多信息，请阅读Java文档或查看[GitHub](https://github.com/Livefyre/livefyre-java-utils)上的源。

## NodeJS {#section_swj_pwq_rz}

要安装NodeJS库，请运行以下行：

`$ npm install livefyre`

NodeJS库依赖于以下模块：

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

有关更多信息，请阅读NodeJs文档或查看[GitHub](https://github.com/Livefyre/livefyre-nodejs-utils)上的源。

链接：[Restler](https://github.com/danwrong/restler)、[Validator](https://www.npmjs.org/package/validator)、[jsonwebtoken](https://github.com/auth0/node-jsonwebtoken)。

## PHP {#section_txj_xwq_rz}

要使用编辑器安装PHP库，请将其添加到您的composer.json中：

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

然后，使用进行安装：

```
composer.phar install 
```

如果&#x200B;**不**&#x200B;使用编辑器，请使用获取库的最新版本：

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

要使用库，请将以下内容添加到PHP脚本中：

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

PHP库依赖于以下模块：

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

有关更多信息，请阅读PHP文档或查看[GitHub](https://github.com/Livefyre/livefyre-php-utils)上的源。

链接：[ext-json](https://www.php.net/manual/en/book.json.php)、[请求](https://github.com/rmccue/Requests/)、[PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

要安装Python库，请运行以下行：

`$ pip install livefyre`

Python库依赖于以下模块：

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

有关更多信息，请阅读Python文档或查看[GitHub](https://github.com/Livefyre/livefyre-python-utils)上的源。

链接：[PyJWT](https://github.com/progrium/pyjwt)、[请求](https://github.com/kennethreitz/requests)、[Python-Dateutil](https://pypi.python.org/pypi/python-dateutil)、[Enum34](https://pypi.python.org/pypi/enum34)、[OrderedDict](https://pypi.python.org/pypi/ordereddict)

## 鲁比 {#section_fv2_tzq_rz}

要安装Ruby库，请将此行添加到应用程序的Gemfile中：

```
gem 'livefyre' 
```

或者自行安装：

`$ gem install livefyre`

Ruby库依赖于以下模块：

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

有关更多信息，请阅读Ruby文档或查看[GitHub](https://github.com/Livefyre/livefyre-ruby-utils)上的源。

链接：[Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)、[REST客户端](https://github.com/rest-client/rest-client/)、[可寻址](https://github.com/sporkmonger/addressable)
