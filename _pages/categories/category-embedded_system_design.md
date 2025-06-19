---
title: "임베디드 시스템 설계"
layout: archive
permalink: categories/embedded_system_design
author_profile: true
sidebar_main: true
---

<p>
임베디드 시스템 설계 라는 과목에서 LAB과제를 진행하였습니다. LAB을 진행하면서 겼었던 과정을 여기에 작성하려고 합니다. 해당과목에서 LAB을 진행할 때, 대만의 terasic 사에서 개발한 <a href="https://www.terasic.com.tw/cgi-bin/page/archive.pl?Language=English&No=836" target="_blank">de1-soc board</a>를 사용하였습니다. 
<p>

{% assign posts = site.categories.['임베디드 시스템 설계'] %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}

