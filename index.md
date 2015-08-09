---
layout: page-fullwidth
title: "Welcome to DKPro"
teaser: "DKPro is a community of projects focussing on re-usable Natural Language Processing software."
style: |
  .product .logo {
    float: right;
    width: 64px;
  }

  .product h4 {
    margin-top: 0px;
  }

  table.product {
    border: none !important;
  }

  .product tr {
    background-color: white !important;
  }

  .product td {
    width: 25%;
    min-width: 25%;
  }

  .product td:hover {
    background-color: #efefef;
  }
---

{% include projects.html status='featured' cols='2' %}

{% include projects.html status='regular' cols='4' %}

{% comment %}
#### Other projects you might be interested in

{% include projects.html status='related' cols='4' %}
{% endcomment %}
