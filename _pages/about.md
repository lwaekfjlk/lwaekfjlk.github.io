---
layout: page
permalink: /
title: about
nav: About
description: <a href="http://www.lti.cs.cmu.edu/" class="page-description" target="_blank">Language Technologies Institute</a> • <a href="http://www.cs.cmu.edu/" class="page-description" target="_blank">School of Computer Science</a> • <a href="http://www.cmu.edu/" class="page-description" target="_blank">Carnegie Mellon University</a>
address: <a href="https://www.google.com/maps/place/Gates+Center+for+Computer+Science/@40.4432641,-79.9449469,19.18z/data=!4m5!3m4!1s0x8834f22175d2f3cf:0x963e80aba7fde2d0!8m2!3d40.4435476!4d-79.9446184" class="page-description" target="_blank">5000 Forbes Ave, Pittsburgh, PA 15213</a>
---

<div class="col p-0 pt-4 pb-4">
  <h1 class="title text-left font-weight-bold">Haofei Yu</h1> 
  <h6 class="pb-3 m-0 mb-2" style="font-size: 0.83em;">于昊飞</h6>
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
        Currently, I'm pursuing a Master of Science in Intelligent Information Systems at the
        <a href="http://www.lti.cs.cmu.edu/" target="_blank">Language Technologies Institute</a>,
        <a href="http://www.cs.cmu.edu/" target="_blank">School of Computer Science</a>,
        Carnegie Mellon University.
        </p>

        <p>
        I completed my Bachelor's in Computer Science and Technology at
        <a href="http://ckc.zju.edu.cn/ckcen/" target="_blank">ChuKochen Honors College</a>,
        <a href="https://www.zju.edu.cn/english/" target="_blank">Zhejiang University</a>,
        engaging in NLP research at
        <a href="https://en.westlake.edu.cn/" target="_blank">Westlake University</a>
        and
        <a href="https://ai.tencent.com/ailab/nlp/en/index.html" target="_blank">Tencent AI Lab's NLP Center</a>.
        </p>

        <p>
        At CMU, my research is centered on developing multisensory agents inspired by consciousness theory, under the mentorship of Professors Graham Neubig, Louis-Philippe Morency, and Ruslan Salakhutdinov. These projects span diverse applications such as web navigation, code execution, and social interaction. Additionally, I've collaborated with Prof. David Mortensen on the linguistic wug test.
        </p>



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
