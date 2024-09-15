---
layout: page
permalink: /
title: about
nav: About
description: <a href="https://siebelschool.illinois.edu" class="page-description" target="_blank">Siebel School of Computing and Data Science</a> • <a href="https://illinois.edu" class="page-description" target="_blank">University of Illinois Urbana-Champaign</a>
address: <a href="https://maps.app.goo.gl/DjM78WnuPHuYT8636" class="page-description" target="_blank">2111A, 201 N Goodwin Ave, Urbana, IL 61801</a>
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
    <section class="profile">
        <!-- Avoid inline styles where possible and use a separate CSS file or <style> block -->
        <div class="profile-image-container">
            <!-- Use alt attribute for accessibility and descriptive image names -->
            <img class="profile-img" src="{{ '/assets/img/self_pic_2.jpg' | prepend: site.baseurl | prepend: site.url }}" alt="Profile Picture">
            <figcaption class="profile-caption" style="font-size: 0.83em;">Taken at Göreme, Cappadocia, Turkey</figcaption>
        </div>

        <!-- Use <p> tag for paragraphs instead of <br> for better semantics and readability -->
        <p>
            I am currently a 1-year Computer Science PhD student at University of Illinois Urbana-Champaign advised by <a href="https://cs.stanford.edu/people/jiaxuan/" target="_blank" rel="noopener">Jiaxuan You</a>. I also work closely with <a href="https://pliang279.github.io/" target="_blank" rel="noopener">Paul Pu Liang</a>. My main research interests lie in language agents and automatic research.
        </p>

        <p>
            Before UIUC, I got my B.Eng. degree in Computer Science (with honors) at
            <a href="http://ckc.zju.edu.cn/ckcen/" target="_blank" rel="noopener">ChuKochen Honors College</a> of
            <a href="https://www.zju.edu.cn/english/" target="_blank" rel="noopener">Zhejiang University</a>. Afterwards, I got my M.S. in Intelligent Information Systems in <a href="https://www.lti.cs.cmu.edu"  target="_blank" rel="noopener">Language Technologies Institute</a> of <a href="https://www.cs.cmu.edu"  target="_blank" rel="noopener">School of Computer Science</a> at Carnegie Mellon University.
        </p>

        <p>
            I have multiple industrial internship experiences including <a href="https://ai.tencent.com/ailab/en/about/" target="_blank" rel="noopener">Tencent AI Lab</a> (2022 Summer), <a href="https://www.apple.com/siri/" target="_blank" rel="noopener">Apple Siri Information and Intelligence Team</a> (2023 Summer), and <a href="https://mitibmwatsonailab.mit.edu" target="_blank" rel="noopener">MIT-IBM Watson AI Lab</a> (2024 Summer). All focusing on language modeling and its applications (long-context, QA, agents).
        </p>

    </section>
</div>

<!-- Add CSS (either inline or preferably in a separate stylesheet) -->
<style>
.profile {
    padding: 0;
}
.profile-image-container {
    display: flex;
    flex-direction: column;
    justify-content: center; /*Center horizontally */
    align-items: center;     /* Center vertically*/
    max-width: 100%;
    padding-top: 0.5rem;
    padding-bottom: 1.5rem;
}
.profile-img {
    width: 100%;
    height: auto; /*to maintain aspect ratio*/
}
.profile-caption {
    text-align: center; /* Centers the text of the caption */
    padding-top: 0.5rem; /* Adds some space between the image and the caption */
    font-style: italic;
    /* Add any additional styling you need for the caption here */
}
@media screen and (max-width: 576px) {
    .profile-image-container {
        max-width: 100%;
        padding-left: 0;
        padding-bottom: 1rem;
    }
}
</style>


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
