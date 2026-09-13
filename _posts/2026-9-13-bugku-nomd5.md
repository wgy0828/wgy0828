---
layout: post
title: "Bugku Crypto 这不是md5"
date: 2026-09-13
categories: CTF
---

## 题目信息
- 平台：Bugku CTF
- 类别：Crypto
- 题目名称：这不是md5
- 作者：harry

## 题目描述
给出一串字符：666c61677b616537333538376261353662616566357d，提示：这不是md5。

## 解题思路
1. 虽然字符串长度和md5一样，但题目明确说了不是md5。
2. 识别为十六进制Hex编码，直接Hex转ASCII。
3. 使用在线十六进制转换器解码得到flag。

## Flag
flag{ae73587ba56baef5}

## 知识点总结
Hex（16进制）编码，字符串长度32位，外观上很像md5哈希，属于CTF经典坑题，看到提示“不是md5”优先尝试hex解码。
