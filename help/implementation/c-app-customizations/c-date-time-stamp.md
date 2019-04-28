---
description: 使用Livefyre. js自定义日期和时间戳。
seo-description: 使用Livefyre. js自定义日期和时间戳。
seo-title: 自定义日期和时间戳
solution: Experience Manager
title: 自定义日期和时间戳
uuid: 632ea405-56b7-4664-8d2b-0dd0a7611bd8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 自定义日期和时间戳{#customize-the-date-and-time-stamp}

使用Livefyre. js自定义日期和时间戳。

Livefyre应用程序提供选项参数DateTimeFormat，以指定如下所述的日期格式。

* [术语](#c_date_time_stamp/section_xsk_jn4_xz)
* [格式化](#c_date_time_stamp/section_ynx_gn4_xz)
* [符号指定](#c_date_time_stamp/section_inq_2n4_xz)

## 术语 {#section_xsk_jn4_xz}

* **绝对时间戳** 定义为精确和特定时间(例如，2012年月日12：00pm)
* **相对时间戳** 定义为一般和不准确的时间(例如25秒前、14分钟前、前一天、年前等)。

## 格式化 {#section_ynx_gn4_xz}

在未给出参数时，dateTimeFormat参数具有以下默认行为：

* 数据时间格式：MMMM d yyyy(2012年月日)
* 20160分钟(14天)直到绝对时间(直到相对时间戳变为绝对时间戳)

dateTimeFormat参数接受三种可能的参数类型：datetime、format和string。

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

指定CompositeFormat和/或searchTesuntibresultTime的对象。值为-1的sundesUntilabsolutiTime将使时间绝对缩短时间。

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

作为参数一个Date对象的函数，返回要显示的datetime字符串

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

按照JDK、ICU和CLDR中定义的模式规范执行数据时间格式设置功能，并对JS中典型使用情况进行少量修改。有关详细信息，请参阅 [Google闭包库文档](https://developers.google.com/closure/library/docs/overview)。

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

标记为&#39;*&#39;的项目尚不受支持。

标有“#”的项目与Java的工作方式不同。

图案字母的计数决定了格式。

* **文本：** 或更多，使用完整表单。少于4，如果存在，则使用简短或缩写的表单。(例如：“EEE”生成“星期一”，“EEE”生成“Mon”。)
* **数字：** 最少位数。较短的数字将零填充为此金额(例如：如果“m”生成“6”，则“mm”生成“06”。)一年专门处理；也就是说，如果“y”的计数为2，则“年”将被截断为位数字。(例如：如果“yyyy”生成“1997”，则“yy”生成“97”。)与其他字段不同，分数秒将在右边添加零秒。
* **文本和号码：** 或以上，使用文本。少于3，使用数字。(例如：“M”生成“1”，“MM”生成“01”，“MMM”生成“Jan”，“MMMM”生成“月”。)

模式中不存在 [的任何字符。&#39;&#39;&#39;&#39;z&#39;] 和 [&#39;A&#39;.&#39;&#39;&#39;&#39;Z&#39;] 将视为带引号的文本。例如，字符“：&#39;，&#39;。&#39;、&#39;、&#39;#&#39;和&#39;@&#39;将显示在生成的时间文本中，即使它们不在单引号中也不接受。
