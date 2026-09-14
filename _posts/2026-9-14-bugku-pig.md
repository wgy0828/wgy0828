---
layout: post
title: "Bugku Crypto 把猪困在猪圈里"
date: 2026-09-14
categories: CTF
---

## 题目信息
- 平台：Bugku CTF
- 类别：Crypto
- 题目名称：把猪困在猪圈里
- 题目ID：159

## 题目描述
下载附件file.txt，文件内为一长串base64编码，题目名称提示猪圈密码。

## 解题步骤
1. 读取附件全部base64字符串，拼接图片前缀：`data:image/jpg;base64,`
2. 使用在线base64转图片工具，将完整字符串转换为图片。
3. 图片中是猪圈密码符号，复制符号使用猪圈密码解密工具解码。
4. 解密得到明文`thisispigpassword`，按格式构造flag。

## Flag
flag{thisispigpassword}
