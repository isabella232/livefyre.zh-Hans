---
description: 此方法返回此集合的URN。 在运行此方法之前，必须运行createOrUpdate()。
title: getUrn收集方法
exl-id: bea04805-8f02-4c06-9a1a-6b057de831ab
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# getUrn收集方法{#geturn-collection-method}

此方法返回此集合的URN。 在运行此方法之前，必须运行createOrUpdate()。

## Java示例{#section_nyl_ycs_rz}

```
collection.getUrn(); 
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## NodeJS示例{#section_xkd_gds_rz}

```
collection.getUrn(); 
```

示例输出：

```
<span class="str">"urn:livefyre:network=`example.fyre.co`:site=1:collection=1"</span>
```

## PHP示例{#section_ghf_gds_rz}

```
$collection->getUrn(); 
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Python示例{#section_dwg_gds_rz}

```
collection.urn() 
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Ruby示例{#section_enh_gds_rz}

```
collection.urn
```

示例输出：

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```
