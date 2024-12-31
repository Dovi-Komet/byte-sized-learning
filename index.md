---
layout: default
title: Python Tutorial
order: 0
---

Welcome to your Python learning journey! This site provides a series of short lessons, starting from the basics and progressing to more advanced topics. Each lesson is designed to be simple, clear, and easy to follow.

## Table of Contents

Below is the list of lessons. Follow the sequence to build your Python skills.

<ul>
  {% assign sorted_pages = site.pages | sort: "order" %}
  {% assign filtered_pages = sorted_pages | where_exp: "item", "item.order != nil" %}
  {% for page in filtered_pages %}
  {% if page.url != "/" %}
  <li><a href="{{ page.url }}">{{ page.title }}</a></li>
  {% endif %}
  {% endfor %}
</ul>

## How to Use This Site
- Each lesson focuses on a specific topic with examples and explanations.
- Follow the lessons in order, as they build upon each other.
- Use the "Next Lesson" button at the bottom of each page to move to the next topic.

Happy coding!
