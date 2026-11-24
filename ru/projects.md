---
layout: default-ru
title: Мои Проекты
---
<div class="page-content">
<p>Список проектов, которыми я хотел бы поделиться с публикой</p>
<div style="display: grid; gap: 25px; margin-top: 20px;">
    {% assign projects = site.ru_projects %}
    {% for project in projects %}
        <div style="background: #f0f2f7; padding: 20px 25px; border-radius: 12px;">
            <h2><a href="{{ project.url }}" style="text-decoration: none; color: #1e2a4a;">{{ project.title }}</a></h2>
            <p>{{ project.content | markdownify | strip_html | truncatewords: 30 }}</p>
            <p><a href="{{ project.url }}">More →</a></p>
        </div>
    {% else %}
        <p>Пока нет проектов.</p>
    {% endfor %}
</div>
</div>