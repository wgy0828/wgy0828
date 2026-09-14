---
layout: post
title: "Bugku Crypto 黄道十二官"
date: 2026-09-14
categories: CTF
---

## 题目信息
- 平台：Bugku CTF
- 类别：Crypto
- 题目名称：黄道十二官
- 题目ID：191

## 题目描述
下载附件图片，图片内为大量特殊符号，复刻真实历史「黄道十二宫杀手Z‑340密码」。

## 解题思路
1. 图片内的符号为Z‑340密码，普通古典密码无法解密。
2. 使用专用解密工具 **AZdecrypt**，将图片中的全部符号手动录入工具。
3. 工具解密得到明文，提取出flag字符串。

## Flag
flag{alphananke}
