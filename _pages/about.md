---
layout: page
permalink: /
title: about
nav: About
description: <a href="http://www.lti.cs.cmu.edu/" class="page-description" target="_blank">Language Technologies Institute</a> • <a href="http://www.cs.cmu.edu/" class="page-description" target="_blank">School of Computer Science</a> • <a href="http://www.cmu.edu/" class="page-description" target="_blank">Carnegie Mellon University</a>
address: <a href="https://www.google.com/maps/place/Gates+Center+for+Computer+Science/@40.4432641,-79.9449469,19.18z/data=!4m5!3m4!1s0x8834f22175d2f3cf:0x963e80aba7fde2d0!8m2!3d40.4435476!4d-79.9446184" class="page-description" target="_blank">5704 Darlington Road, Pittsburgh, PA 15217</a>
---

<div class="col p-0 pt-4 pb-4">
  <h1 class="title text-left font-weight-bold">Haofei Yu</h1> 
  <h6 class="pb-3 m-0 mb-2" style="font-size: 0.83em;">Humphrey | 于昊飞</h6>
  <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.description }}</h6>
  {% if page.address %}
      <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.address }}</h6>
  {% endif %}
</div>


<!-- Introduction -->

<div style="display: flex; flex-wrap: wrap;">
    <div class="text-justify p-0">
        <div class="col-xs-12 col-sm-6 p-0 pt-2 pb-sm-2 pb-4 pl-sm-4 text-center" style="float: right;">
          <img class="profile-img img-responsive" src="{{ 'self_pic.jpg' | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}">
        </div>

        <p>
        I am currently a first year MIIS (Master of Science in Intelligent Information Systems) student in the <a href="http://www.lti.cs.cmu.edu/" target="_blank">Language Technologies Institute</a>, <a href="http://www.cs.cmu.edu/" target="_blank">School of Computer Science</a> at <a href="http://www.cmu.edu/" target="_blank">Carnegie Mellon University</a>.
        </p>

        <p>
        Prior to CMU, I obtained my BEng's degree of Computer Science and Technology from <a href="http://ckc.zju.edu.cn/ckcen/" target="_blank">ChuKochen Honors College</a>, <a href="https://www.zju.edu.cn/english/" target="_blank">Zhejiang University</a> in China.
        During my undergraduate studies, I was a member of the Mixed Class of 2022 and felt honoured to participate in NLP research at <a href="https://en.westlake.edu.cn/" target="_blank">Westlake University</a> and <a href="https://ai.tencent.com/ailab/nlp/en/index.html" target="_blank">Tencent AI Lab (NLP Center)</a>.
        </p>

        <p>
        Different types of generation tasks, such as dialogue generation, question answering, language modeling, and code generation, are of particular interest to me. Generally speaking, I am curious about designing task-specific methods to help model better comprehend dynamic semantic information (on the encoder side) and produce complex outcomes (on the decoder side) in seq2seq generation framework.
        </p>

        Refer to my resume <a class="ml-auto mr-2" href="/assets/pdf/resume.pdf" target="_blank"><img height="25px" src="/assets/img/pdf_icon.svg"></a>for more details, lastest update on <i>Aug 31, 2022</i>.


    </div>
</div>


<!-- News -->
<div class="news mt-3 p-0">
  <h3 class="title mb-4 p-0">News</h3>
  {% assign news = site.news | reverse %}
  {% for item in news limit: site.news_limit %}
    <div class="row p-0">
      <div class="col-sm-2 p-0">
        <span class="badge danger-color-dark darken-1 font-weight-bold text-uppercase align-middle date ml-3">
          {{ item.date | date: "%b %-d, %Y" }}
        </span>
      </div>
      <div class="col-sm-10 mt-2 mt-sm-0 ml-3 ml-md-0 p-0 font-weight-light text">
        <p>{{ item.content | remove: '<p>' | remove: '</p>' | emojify }}</p>
      </div>
    </div>
  {% endfor %}
</div>

<script type="text/javascript" id="clustrmaps" src="//cdn.clustrmaps.com/map_v2.js?cl=ffffff&w=700&t=tt&d=NhXj4joI7G-QcI07Qz4cPPkmnIj_bE-Zi4HhgEt-oCs"></script>
