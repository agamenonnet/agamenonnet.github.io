---
layout: index
title: "Investindo com Agamenon"
---

_**Disclaimer:** As opiniões expressas neste site são exclusivamente pessoais e não devem ser interpretadas como conselhos financeiros ou recomendações de investimento. Não possuo formação na área financeira e não me responsabilizo por quaisquer decisões tomadas com base nas informações apresentadas. Este espaço é dedicado a compartilhar reflexões e experiências pessoais._

<ul>
  {% for page in site.pages %}
    {% if page.title and page.url != "/" %}
      <li>
        <a href="{{ page.url }}">{{ page.title }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>

## Diário do investidor

<ul>
  {% for post in site.categories.diario %}
    <li>
      {{ post.date | date: "%d %b %Y" | replace: "Jan", "Jan" | replace: "Feb", "Fev" | replace: "Mar", "Mar" | replace: "Apr", "Abr" | replace: "May", "Mai" | replace: "Jun", "Jun" | replace: "Jul", "Jul" | replace: "Aug", "Ago" | replace: "Sep", "Set" | replace: "Oct", "Out" | replace: "Nov", "Nov" | replace: "Dec", "Dez" }} <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


## Blog

<ul>
  {% for post in site.posts %}
  {% unless post.categories contains "diario" %}
    <li>
      {{ post.date | date: "%d %b %Y" | replace: "Jan", "Jan" | replace: "Feb", "Fev" | replace: "Mar", "Mar" | replace: "Apr", "Abr" | replace: "May", "Mai" | replace: "Jun", "Jun" | replace: "Jul", "Jul" | replace: "Aug", "Ago" | replace: "Sep", "Set" | replace: "Oct", "Out" | replace: "Nov", "Nov" | replace: "Dec", "Dez" }} <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endunless %}
  {% endfor %}
</ul>
