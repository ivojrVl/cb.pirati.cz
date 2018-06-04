---
layout: default
section: blog
description: Stránka českobudějovické pirátské buňky s nejnovějšími články a základním rozcestníkem. 
keywords: organizace, transparence, politika
---

{% include title_hero.html %}

<div class="container homepage is">

  <div class="row">
    <div class="col-sm-12 col-lg-6">
      <section id="posts">
      {% for post in site.posts limit:2 %}
        <div class="column">
        {% include shared/articlesumary.html %}
        </div>
      {% endfor %}
        <h4><a href="/clanky/">Ostatní články ...</a></h4>
      </section>

      <section id="akce" class="mt-3">
        <h2>nejbližší akce</h2>

        {% for item in site.data.akce limit:3 %}
        {% include shared/eventsummary.html item=item %}
        {% endfor %}

      </section>

    </div>

    <div class="col-sm-12 col-lg-6">
      {% include rightbar.html %}
    </div>
  </div>

</div>
