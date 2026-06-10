---
layout: page
permalink: /
title: about
nav: About
description: <a href="https://siebelschool.illinois.edu" class="page-description" target="_blank">Siebel School of Computing and Data Science</a> &bull; <a href="https://illinois.edu" class="page-description" target="_blank">University of Illinois Urbana-Champaign</a>
address: <a href="https://maps.app.goo.gl/DjM78WnuPHuYT8636" class="page-description" target="_blank">2119B, 201 N Goodwin Ave, Urbana, IL 61801</a>
---

<!-- Profile Header -->
<div class="profile-header">
  <h1 class="profile-name">Haofei Yu</h1>
  <p class="profile-name-cn">于昊飞</p>
  <p class="profile-affiliation">{{ page.description }}</p>
  {% if page.address %}
  <p class="profile-address">{{ page.address }}</p>
  {% endif %}
  <div class="profile-links">
    <a href="mailto:{{ site.email }}" title="Email"><i class="fa fa-envelope"></i> Email</a>
    <a href="https://scholar.google.com/citations?userid={{ site.scholar_userid }}&user={{ site.scholar_userid }}" target="_blank" rel="noopener" title="Google Scholar"><i class="ai ai-google-scholar"></i> Scholar</a>
    <a href="https://www.github.com/{{ site.github_username }}" target="_blank" rel="noopener" title="GitHub"><i class="fab fa-github"></i> GitHub</a>
    <a href="https://www.linkedin.com/in/{{ site.linkedin_username }}" target="_blank" rel="noopener" title="LinkedIn"><i class="fab fa-linkedin"></i> LinkedIn</a>
    <a href="https://x.com/{{ site.twitter_username }}" target="_blank" rel="noopener" title="X"><svg class="x-logo-icon" viewBox="0 0 24 24" aria-hidden="true"><path d="M18.901 1.153h3.68l-8.04 9.19L24 22.846h-7.406l-5.8-7.584-6.638 7.584H.474l8.6-9.83L0 1.154h7.594l5.243 6.932ZM17.61 20.644h2.039L6.486 3.24H4.298Z"/></svg> X</a>
  </div>
</div>

<!-- Photo -->
<div class="photo-section">
  <img src="{{ '/assets/img/self_pic_2.jpg' | prepend: site.baseurl | prepend: site.url }}" alt="Haofei Yu">
  <figcaption class="photo-caption">Taken at <a href="https://en.wikipedia.org/wiki/G%C3%B6reme" target="_blank" rel="noopener">Goreme</a>, Cappadocia, Turkey. Credit to <a href="https://zns77.github.io/" target="_blank" rel="noopener">Naisong</a>.</figcaption>
</div>

<!-- Bio -->
<div class="bio-section">
  <p>
    I am currently a second-year PhD student at <a href="https://siebelschool.illinois.edu/" target="_blank" rel="noopener">Siebel School of Computing and Data Science</a>, <a href="https://illinois.edu/" target="_blank" rel="noopener">University of Illinois Urbana-Champaign</a> advised by <a href="https://cs.stanford.edu/people/jiaxuan/" target="_blank" rel="noopener">Jiaxuan You</a>. I also work closely with <a href="https://pliang279.github.io/" target="_blank" rel="noopener">Paul Pu Liang</a>. My main research interests lie in reinforcement learning and world modeling.
  </p>

  <p>
    Before UIUC, I got my B.Eng. degree in Computer Science (with honors) at
    <a href="http://ckc.zju.edu.cn/ckcen/" target="_blank" rel="noopener">ChuKochen Honors College</a> of
    <a href="https://www.zju.edu.cn/english/" target="_blank" rel="noopener">Zhejiang University</a>. Afterwards, I got my M.S. in Intelligent Information Systems in <a href="https://www.lti.cs.cmu.edu" target="_blank" rel="noopener">Language Technologies Institute</a> of <a href="https://www.cs.cmu.edu" target="_blank" rel="noopener">School of Computer Science</a> at <a href="https://www.cmu.edu/" target="_blank" rel="noopener">Carnegie Mellon University</a>.
  </p>

  <p>
    I have multiple industrial internship experiences including <a href="https://ai.tencent.com/ailab/en/about/" target="_blank" rel="noopener">Tencent AI Lab</a> (2022), <a href="https://www.apple.com/siri/" target="_blank" rel="noopener">Apple Siri Information and Intelligence Team</a> (2023), <a href="https://mitibmwatsonailab.mit.edu" target="_blank" rel="noopener">MIT-IBM Watson AI Lab</a> (2024), <a href="https://allenai.org/" target="_blank" rel="noopener">Allen Institute for AI (Ai2)</a> (2025), and <a href="https://ai.meta.com/" target="_blank" rel="noopener">Meta AI</a> (2026). All focusing on language modeling and its applications.
  </p>
</div>


<!-- Publications -->
<div class="publications mt-3 p-0">
  <h2 class="section-title">Publications</h2>

  <!-- Papers list -->
  {% for paper in site.data.papers %}
    <div class="paper-item">
      <div class="paper-info">
        {% if paper.links.paper %}
        <a href="{{ paper.links.paper }}" class="paper-title" target="_blank" rel="noopener noreferrer">
          {{ paper.title }}
        </a>
        {% else %}
        <span class="paper-title">{{ paper.title }}</span>
        {% endif %}
        <div class="paper-authors">
          {% for author in paper.authors %}{% if author contains "Haofei Yu" %}<strong>{{ author }}</strong>{% else %}{{ author }}{% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}
        </div>
        <div class="venue">{{ paper.venue }}</div>
        <div class="paper-links">
          {% if paper.links.paper %}
            <a href="{{ paper.links.paper }}" target="_blank" rel="noopener noreferrer" class="paper-link">[Paper]</a>
          {% endif %}
          {% if paper.links.code %}
            <a href="{{ paper.links.code }}" target="_blank" rel="noopener noreferrer" class="paper-link">[Code]</a>
          {% endif %}
          {% if paper.links.data %}
            <a href="{{ paper.links.data }}" target="_blank" rel="noopener noreferrer" class="paper-link">[Data]</a>
          {% endif %}
          {% if paper.links.model %}
            <a href="{{ paper.links.model }}" target="_blank" rel="noopener noreferrer" class="paper-link">[Model]</a>
          {% endif %}
          {% if paper.links.media %}
            <a href="{{ paper.links.media }}" target="_blank" rel="noopener noreferrer" class="paper-link">[Media]</a>
          {% endif %}
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<!-- Visitor Map -->
<div class="visitor-map mt-4 p-0" style="text-align: center;">
  <script type="text/javascript" id="clustrmaps" src="https://cdn.clustrmaps.com/map_v2.js?cl=ffffff&w=700&t=tt&d=NhXj4joI7G-QcI07Qz4cPPkmnIj_bE-Zi4HhgEt-oCs"></script>
</div>
