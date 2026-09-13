---
layout: post
title: "Bugku MISC linux"
date: 2026-09-13
categories: CTF
---

## 题目信息
- 平台：Bugku CTF
- 类别：MISC杂项
- 题目名称：linux
- 提示：key{}
- 描述：linux基础问题

## 解题思路
1. 下载附件压缩包，进行两次解压，得到二进制文件flag。
2. 该文件是二进制，打开大部分是乱码，直接搜索字符串关键词`key`。
3. Linux下使用 `strings flag | grep key` 提取字符串；Windows可用Notepad++打开，Ctrl+F搜索key。
4. 找到结果，格式为`key{...}`，直接提交。

## Key
key{feb81d3834e2423c9903f4755464060b}

## 知识点总结
1. strings命令：提取二进制文件里所有可读字符串，MISC常用工具。
2. 二进制文件里嵌入明文字符串，直接搜索关键词即可拿到答案。
