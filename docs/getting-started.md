---
title: Getting started
---


In this category i will mention some necessary and quality of life features.


To change the announcement bar content at the top you need to change `material/overrides/main.html`

change the following:

``` html hl_lines="9 10 11"
{#-
  This file was automatically generated - do not edit
-#}
{% extends "base.html" %}
{% block extrahead %}
  <link rel="stylesheet" href="{{ 'assets/stylesheets/custom.css' | url }}">
{% endblock %}
{% block announce %}
  <div class="announce_text">
    Some info and updates here!
  </div>
{% endblock %}
{% block scripts %}
  {{ super() }}
  <script src="{{ 'assets/javascripts/custom.js' | url }}"></script>
{% endblock %}

```

Change `Some info and updates here!`.

Every time this announcement has changed the bar will reapear if people have clicked it away.<br>
_(it will stay hidden until this file has been changed)_

