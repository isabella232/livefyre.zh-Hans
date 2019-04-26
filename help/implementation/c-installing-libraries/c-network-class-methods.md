---
description: 创建网络对象。
seo-description: 创建网络对象。
seo-title: 网络类方法
solution: Experience Manager
title: 网络类方法
uuid: 4130beda-dd09-49ae-aafb-f6 b956 e30 b51
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 网络类方法{#network-class-methods}

创建网络对象。

创建网络对象后，页面的其余部分将假定您的会话中有一个实例化的网络对象。

## 网络对象

| 参数 | Type | 描述 |
|---|---|---|
| *`network`* | 字符串 | 您的Livefyre网络。例如：`labs.fyre.co`。 |
| *`networkKey`* | 字符串 | Livefyre为网络提供的机密密钥。 |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## NodeJS {#section_nyk_dzs_kbb}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork(network, networkKey); 
```

## PHP {#section_oyk_dzs_kbb}

```
use Livefyre\Livefyre; 
  
$network = Livefyre::getNetwork(network, networkKey); 
```

## Python {#section_pyk_dzs_kbb}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network(network, networkKey) 
```

## Ruby {#section_qyk_dzs_kbb}

```
require 'livefyre' 
  
network = Livefyre.get_network(network, networkKey) 
```
