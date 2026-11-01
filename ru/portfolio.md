---
layout: default-ru
title: Портфолио
permalink: /ru/portfolio/
---

<h1>Портфолио работ</h1>

<div class="portfolio-grid">
    {% assign works = site.ru_portfolio | sort: "title", "last" %}
    {% for work in works %}
        <div class="portfolio-card">
            <h3>{{ work.title }}</h3>
            <p class="description">{{ work.description | truncatewords: 10 }}</p>
            
            {% if work.tags %}
                <div class="tags">
                    {% for tag in work.tags %}
                        <span class="tag">{{ tag | strip }}</span>
                    {% endfor %}
                </div>
            {% endif %}
            
            <a href="{{ work.url }}" class="read-more">Подробнее →</a>
        </div>
    {% else %}
        <p>Пока нет работ в портфолио.</p>
    {% endfor %}
</div>