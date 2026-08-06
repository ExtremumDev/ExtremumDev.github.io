---
layout: default-ru
title: Проекты
---
<div class="page-content">
<p>Список проектов, ходом разработки которых я захотел поделиться</p>
<p>Каждый проект состоит из описания(цель, суть, на чём разрабатывается), ссылок на проект(репозиторий или на сам продукт) и список логов(публикаций, которые делаю по ходу работы над проектом, фиксирующих какие-то важные изменения, архитектурные решения или просто новости)</p>

<div style="display: grid; gap: 25px; margin-top: 20px;">
    {% assign projects = site.ru_projects %}
    {% for project in projects %}
        <div style="background: #f0f2f7; padding: 20px 25px; border-radius: 12px;">
            <h2><a href="{{ project.url }}" style="text-decoration: none; color: #1e2a4a;">{{ project.title }}</a></h2>
            <p>{{ project.content | markdownify | strip_html | truncatewords: 30 }}</p>
            <p><a href="{{ project.url }}">Подробнее →</a></p>
        </div>
    {% else %}
        <p>Пока нет проектов.</p>
    {% endfor %}
</div>
</div>