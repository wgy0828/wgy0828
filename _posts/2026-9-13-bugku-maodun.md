---
layout: post
title: "Bugku Web 矛盾"
date: 2026-09-13
categories: CTF
---

## 题目信息
- 平台：Bugku CTF
- 类别：Web PHP弱类型
- 题目名称：矛盾

## 题目源码
```php
$num=$_GET['num'];
if(!is_numeric($num))
{
    echo $num;
    if($num==1)
    echo 'flag{**********}';
}

## 题目分析

存在两个看起来互相矛盾的条件：

1. !is_numeric($num)：变量不能是数字，才可以进入代码块。
2. $num == 1：变量弱等于数字1。

PHP弱类型特性：

• is_numeric()遇到字符串末尾带空字节\0时返回false；
• 使用==弱比较时，"1\0"会被转换成数字1，满足$num ==1。

Payload
?num=1%00
完整访问示例：
http://160.202.254.160:18009/?num=1%00

## 解题步骤

1. 在url后面拼接GET参数 ?num=1%00
2. 访问页面，网页输出flag
3. 复制页面返回的flag提交

## Flag
flag{f6776449a03ad31e9f8bae1e2751a364}

## 知识点总结

1. PHP is_numeric() 检测数字字符串，空字节%00会让判断失效。
2. == 是弱相等，会自动进行类型转换，和===强严格相等有本质区别。
3. URL编码 %00 代表空字节\0。
