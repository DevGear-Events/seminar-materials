---
layout: page
title: 2026-03-11 세미나 자료
description: ""  # 이 부분을 추가하면 상단에 본문 첫 줄이 나오는 것을 막을 수 있습니다.
---

## 📂 발표 자료 및 소스코드

<ul>
  {% assign current_dir = page.url | remove: "index.html" %}
  {% for file in site.static_files %}
    {% if file.path contains current_dir %}
      {% unless file.path contains "index.md" or file.path contains "README.md" %}
        <li>
          <a href="{{ site.baseurl }}{{ file.path }}" target="_blank">
            {{ file.name }} 
            <small>({{ file.extname | remove: "." | upcase }})</small>
          </a>
        </li>
      {% endunless %}
    {% endif %}
  {% endfor %}
</ul>

---
[← 목록으로 돌아가기]({{ site.baseurl }}/)
