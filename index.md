---
layout: page-fullwidth
title: "Welcome"
teaser: "DKPro is a community of projects focussing on re-usable Natural Language Processing software."
style: |
  ._product ._logo {
    float: right;
    width: 64px;
    margin: 0.5em;
  }

  ._product ._name {
    padding: 0.5em;
    font-size: 125%;
    background-color: #efefef;
    border-radius:0.25em;
  }

  ._product ._description {
    margin: 0.5em;
  }
---

{% include projects.html status='featured' cols='2' %}

----

{% include projects.html status='regular' cols='3' %}

----

Here are a few additional projects which are not part of DKPro proper, but which are closely related,
compatible  with DKPro products and building on them.

{% include projects.html status='related' cols='3' %}

{% comment %}
#### Other projects you might be interested in

{% include projects.html status='related' cols='4' %}
{% endcomment %}
