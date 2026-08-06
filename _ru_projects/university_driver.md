---
layout: default-ru
title: Мой крутой проект
project_slug: university_driver   # тот же ключ, что и в логах
lang: ru
---
## О проекте

Текст описания...

## Логи изменений

{% assign project_logs = site.logs | where: "project_slug", page.project_slug | where: "lang", page.lang | sort: "date" | reverse %}

{% if project_logs.size > 0 %}
  <ul>
    {% for log in project_logs %}
      <li>
        <strong>{{ log.date | date: "%d.%m.%Y" }}</strong> — 
        <a href="{{ log.url }}">{{ log.title }}</a>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p>Логов пока нет.</p>
{% endif %}