---
description: 使用Livefyre.js自定义日期和时间戳。
seo-description: 使用Livefyre.js自定义日期和时间戳。
seo-title: 自定义日期和时间戳
solution: Experience Manager
title: 自定义日期和时间戳
uuid: 632ea405-56b7-4664-8d2b-0dd0a7611bd8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 自定义日期和时间戳{#customize-the-date-and-time-stamp}

使用Livefyre.js自定义日期和时间戳。

Livefyre应用程序提供选项参数datetimeFormat，用于指定日期格式，如下所述。

* [术语](#c_date_time_stamp/section_xsk_jn4_xz)
* [格式化](#c_date_time_stamp/section_ynx_gn4_xz)
* [符号指定](#c_date_time_stamp/section_inq_2n4_xz)

## 术语 {#section_xsk_jn4_xz}

* **绝对时间戳** ，定义为精确时间和特定时间（例如，2012年1月1日12:00pm）
* **相对时间戳** (Relative Timestamps)定义为一般时间，且不太精确（例如，25秒前、14分钟前、1天前、1年前等）

## 格式化 {#section_ynx_gn4_xz}

当没有给定参数时，datetimeFormat参数具有以下默认行为：

* 日期时间格式：MMMMM d yyyy（2012年1月8日）
* 20160分钟（14天），直到绝对时间（14天，直到相对时间戳变为绝对时间戳）

datetimeFormat参数接受三种可能的参数类型：datetime、format和string。

```
// Example 1 (Datetime format string)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": 'MMM d y Ka' 
}; 
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

指定absoluteFormat和／或minutesUntilAbsoluteTime的对象。 值为-1的minutesUntilAbsoluteTime将使时间绝对时间立即生效。

```
// Example 2 (Object)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": { 
      minutesUntilAbsoluteTime: 10, 
      absoluteFormat: 'MMM d y Ka' 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

将Date对象作为参数并返回要显示的日期时间字符串的函数

```
// Example 3 (Function accepting a Date object, returning a datetime string to display) 
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": function(theDateInput) { 
      return +theDateInput; 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

## 符号指定 {#section_inq_2n4_xz}

按照JDK、ICU和CLDR中定义的模式规范进行日期时间格式设置功能，对JS中的典型用法稍作修改。 有关详细信息，请参 [阅Google Closure库文档](https://developers.google.com/closure/library/docs/overview)。

```
  Symbol Meaning Presentation        Example 
  ------   -------                 ------------        ------- 
  G        era designator          (Text)              AD 
  y#       year                    (Number)            1996 
  Y* year (week of year)     (Number)            1997 
  u* extended year           (Number)            4601 
  M        month in year           (Text & Number)     July & 07 
  d        day in month            (Number)            10 
  h        hour in am/pm (1~12)    (Number)            12 
  H        hour in day (0~23)      (Number)            0 
  m        minute in hour          (Number)            30 
  s        second in minute        (Number)            55 
  S        fractional second       (Number)            978 
  E        day of week             (Text)              Tuesday 
  e* day of week (local 1~7) (Number)            2 
  D* day in year             (Number)            189 
  F* day of week in month    (Number)            2 (2nd Wed in July) 
  w* week in year            (Number)            27 
  W* week in month           (Number)            2 
  a        am/pm marker            (Text)              PM 
  k        hour in day (1~24)      (Number)            24 
  K        hour in am/pm (0~11)    (Number)            0 
  z        time zone               (Text)              Pacific Standard Time 
  Z        time zone (RFC 822)     (Number)            -0800 
  v        time zone (generic)     (Text)              Pacific Time 
  g* Julian day              (Number)            2451334 
  A* milliseconds in day     (Number)            69540000 
  '        escape for text         (Delimiter)         'Date=' 
  ''       single quote            (Literal)           'o''clock'
```

尚不支持标有“*”的项目。

标有“#”的项目的工作方式与Java不同。

模式字母的计数决定格式。

* **** 文本：4或更多，请使用完整表单。 少于4，如果存在，请使用短或缩写表单。 (例如：“EEE”生成“星期一”,“EEE”生成“星期一”。)
* **** 数字：最小数字数。 较短的数字将填充为此数量(例如：如果“m”生成“6”，则“mm”生成“06”。) 具体处理年份；即，如果“y”的计数为2，则“年”将截断为2位数。 (例如：如果“yyyy”生成“1997”，则“yy”生成“97”。)与其他字段不同，分数秒在右边填充为零。
* **** 文本和编号：3或更多，使用文本。 少于3，使用号。 (例如：“M”生成“1”,“MM”生成“01”,“MMM”生成“Jan”,“MMM”生成“Jan”。)

图案中不在“a”...”范围 [内的任何字符z’] and [‘A’...’Z将被视] 为带引号的文本。 例如，“:”、“.”、“‘,#’和“@”等字符将显示在生成的时间文本中，即使它们没有用在单引号中也是如此。
