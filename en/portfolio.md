---
layout: default-en
title: Portfolio
permalink: /en/portfolio/
---

<h1>My projects / completed works</h1>

<div class="portfolio-grid">
    {% assign works = site.en_portfolio | sort: "title", "last" %}
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
            
            <a href="{{ work.url }}" class="read-more">More →</a>
        </div>
    {% else %}
        <p>There are no projects yes.</p>
    {% endfor %}
</div>