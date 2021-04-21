---
description: 创建Network对象。
title: 网络类方法
exl-id: 5a011120-05d0-4768-9038-6a312e8c5dd1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 11%

---

# 网络类方法{#network-class-methods}

创建Network对象。

创建网络对象后，页面的其余部分将假设您的会话中有一个实例化的Network对象。

## 网络对象

| 参数 | 类型 | 描述 |
|---|---|---|
| *`network`* | 字符串 | 您的Livefyre网络。 例如：&quot;`labs.fyre.co`&quot;。 |
| *`networkKey`* | 字符串 | Livefyre为网络提供的密钥。 |

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

## 拼音{#section_qyk_dzs_kbb}

```
require 'livefyre' 
  
network = Livefyre.get_network(network, networkKey) 
```
