---
layout: default
title: wgy0828的博客
---

# 欢迎来到我的个人空间！

共同进步！

---

## 最新文章

<ul>
  {% for post in site.posts %}
    <li style="margin-bottom: 15px;">
      <!-- 核心：a标签才是真正的超链接 -->
      <a href="{{ post.url }} " style="font-size: 18px; color: #0366d6; text-decoration: none;">{{ post.title }}</a >
      <br>
      <small style="color: #888;">{{ post.date | date: "%Y-%m-%d" }}</small>
    </li>
  {% endfor %}
</ul>
