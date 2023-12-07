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
    <section class="profile">
        <!-- Avoid inline styles where possible and use a separate CSS file or <style> block -->
        <div class="profile-image-container">
            <!-- Use alt attribute for accessibility and descriptive image names -->
            <img class="profile-img" src="{{ '/assets/img/self_pic_2.jpg' | prepend: site.baseurl | prepend: site.url }}" alt="Profile Picture">
        </div>

        <!-- Use <p> tag for paragraphs instead of <br> for better semantics and readability -->
        <h4>Background</h4>
        <p>
            I am currently in the second year at Carnegie Mellon University, pursuing a Master of Science in Intelligent Information Systems within the 
            <a href="http://www.lti.cs.cmu.edu/" target="_blank" rel="noopener">Language Technologies Institute</a> of the 
            <a href="http://www.cs.cmu.edu/" target="_blank" rel="noopener">School of Computer Science</a>.
        </p>

        <p>
            Before my journey at CMU, I laid my academic foundations at the
            <a href="http://ckc.zju.edu.cn/ckcen/" target="_blank" rel="noopener">ChuKochen Honors College</a> of
            <a href="https://www.zju.edu.cn/english/" target="_blank" rel="noopener">Zhejiang University</a>, where I obtained my Bachelor's degree in Computer Science and Technology (with honors). During my years there, I had the privilege of delving into Natural Language Processing (NLP) research, contributing to natural language processing research at
            <a href="https://en.westlake.edu.cn/" target="_blank" rel="noopener">Westlake University</a> and
            <a href="https://ai.tencent.com/ailab/nlp/en/index.html" target="_blank" rel="noopener">Tencent AI Lab's NLP Center</a>.
        </p>

        <p>
            At CMU, my research changing from natural language processing to more interesting and grounded stuff. Instead of doing research on traditional NLP tasks, I studied crafting language agents for better social interaction in negotiation and collaboration scenarios. Additionally, I worked on models that fuse multimodal information and models that generate executable actions like web navigation and code generation. 
        </p>

        <p>
            Moreover, my 2023 summer internship at 
            <a href="https://www.apple.com/siri/" target="_blank" rel="noopener">Apple's Siri Information and Intelligence Team</a> focuses on long-form Web QA to effectively resolve real Siri user queries in industry.
        </p>

        <h4>Research Interest</h4>
        <p>
            My research enthusiasm lies in applying AI to grounded tasks. My primary goal is to develop a multimodal agent tailored for real-world applications, blending the practical with the magical in technology. To achieve this goal, I identified three main challenges: 
        </p>
        <p>
        <strong>Challenge1 Multimodal Fusion</strong> <br>
        How to allow the agent to fuse heterogeneous data and understand multimodal concepts like sarcasm.
        </p>

        <p>
        <strong>Challenge2 Multimodal Interaction</strong> <br>
        How to enable the agent to provide feedback, including language and executable action, to the real world interactively.
        </p>
        
        <p>
        <strong>Challenge3 Memory Management</strong> <br>
        How to equip the agent with a memory system that adapts to new information while retaining past ones.
        </p>

        <p> The following figure is an overview of 3 challenges in the observation-feedback loop for multimodal agent, accompanied by a snapshot of my current research progress on each of them, including ongoing work.</p>

        <div style="display: flex; flex-wrap: wrap; justify-content: center; align-items: center;">
            <!-- Use alt attribute for accessibility and descriptive image names -->
            <img class="profile-img" src="{{ '/assets/img/statement.png' | prepend: site.baseurl | prepend: site.url }}" alt="Research Line">
        </div>
    </section>
</div>

<!-- Add CSS (either inline or preferably in a separate stylesheet) -->
<style>
.profile {
    padding: 0;
}
.profile-image-container {
    display: flex;
    justify-content: center; /*Center horizontally */
    align-items: center;     /* Center vertically*/
    max-width: 100%;
    padding-top: 0.5rem;
    padding-bottom: 2.5rem;
}
.profile-img {
    width: 100%;
    height: auto; /*to maintain aspect ratio*/
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
