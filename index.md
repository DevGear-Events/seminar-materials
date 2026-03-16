---
layout: home
title: 세미나 목록
---

## 📅 세미나별 자료 보기

{% for file in site.static_files %}
  {% if file.path contains '/seminar-' %}
    {% endif %}
{% endfor %}

* [2024 신기술 세미나](./seminar-2024-tech/)
* [Delphi Spring Camp](./seminar-delphi-spring/)

> 각 폴더로 들어가시면 PDF 및 예제 코드를 받으실 수 있습니다.
