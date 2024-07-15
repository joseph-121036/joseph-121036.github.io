---
title: "sophomore"
layout: archive
permalink: categories/sophomore
author_profile: true
sidebar_main: true
---


{% assign posts = site.categories.sophomore %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}
