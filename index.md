---
layout: page
title: 전체 세미나 목록
---

# 📅 세미나 아카이브
새로운 폴더가 추가되면 자동으로 업데이트됩니다.

<ul>
  {% assign static_files = site.static_files | sort: 'path' | reverse %}
  {% assign displayed_dirs = "" %}

  {% for file in static_files %}
    {% if file.path contains '/20' %}
      {% assign parts = file.path | split: '/' %}
      {% assign dir_name = parts[1] %}
      
      {% unless displayed_dirs contains dir_name %}
        <li>
          <a href="{{ site.baseurl }}/{{ dir_name }}/" style="font-weight: bold; font-size: 1.1em;">
            {{ dir_name | replace: 'seminar-', '' | replace: '-', ' ' | upcase }}
          </a>
        </li>
        {% assign displayed_dirs = displayed_dirs | append: dir_name | append: "," %}
      {% endunless %}
    {% endif %}
  {% endfor %}
</ul>
