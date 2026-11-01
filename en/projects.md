
<div class="page-content">
<p>List of projects I am glad to show to the public</p>
<p> Each project's page consists of description(it's goal, core and tech stack), links on the project(e.g. repo) and list of logs(posts done by me during the project development. They commit most important changes, decisions or just news about project)</p>
<div style="display: grid; gap: 25px; margin-top: 20px;">
    {% assign projects = site.en_projects %}
    {% for project in projects %}
        <div style="background: #f0f2f7; padding: 20px 25px; border-radius: 12px;">
            <h2><a href="{{ project.url }}" style="text-decoration: none; color: #1e2a4a;">{{ project.title }}</a></h2>
            <p>{{ project.content | markdownify | strip_html | truncatewords: 30 }}</p>
            <p><a href="{{ project.url }}">More →</a></p>
        </div>
    {% else %}
        <p>No projects yes.</p>
    {% endfor %}
</div>
</div>