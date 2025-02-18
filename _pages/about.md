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
            <figcaption class="profile-caption" style="font-size: 0.83em;">Taken at <a href="https://en.wikipedia.org/wiki/G%C3%B6reme" target="_blank" rel="noopener">Göreme</a>, Cappadocia, Turkey. Credit to <a href="https://zns77.github.io/" target="_blank" rel="noopener">Naisong</a>.</figcaption>
        </div>

        <!-- Use <p> tag for paragraphs instead of <br> for better semantics and readability -->
        <p>
            I am currently a first-year PhD student at <a href="https://siebelschool.illinois.edu/" target="_blank" rel="noopener">Siebel School of Computing and Data Science</a>, <a href="https://illinois.edu/"  target="_blank" rel="noopener">University of Illinois Urbana-Champaign</a> advised by <a href="https://cs.stanford.edu/people/jiaxuan/" target="_blank" rel="noopener">Jiaxuan You</a>. I also work closely with <a href="https://pliang279.github.io/" target="_blank" rel="noopener">Paul Pu Liang</a>. My main research interests lie in language agents and automatic research.
        </p>

        <p>
            Before UIUC, I got my B.Eng. degree in Computer Science (with honors) at
            <a href="http://ckc.zju.edu.cn/ckcen/" target="_blank" rel="noopener">ChuKochen Honors College</a> of
            <a href="https://www.zju.edu.cn/english/" target="_blank" rel="noopener">Zhejiang University</a>. Afterwards, I got my M.S. in Intelligent Information Systems in <a href="https://www.lti.cs.cmu.edu"  target="_blank" rel="noopener">Language Technologies Institute</a> of <a href="https://www.cs.cmu.edu"  target="_blank" rel="noopener">School of Computer Science</a> at <a href="https://www.cmu.edu/" target="_blank" rel="noopener">Carnegie Mellon University</a>.
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
    /* Add any additional styling you need for the caption here */
}
@media screen and (max-width: 576px) {
    .profile-image-container {
        max-width: 100%;
        padding-left: 0;
        padding-bottom: 1rem;
    }
}
.venue {
    font-size: 0.9rem;
    color: #666;
    margin-bottom: 0.5rem;
  }
  
  .paper-links {
    margin-bottom: 0.75rem;
  }
  
  .paper-link {
    display: inline-block;
    margin-right: 0.5rem;
    color: #2196f3;
    text-decoration: none;
    font-size: 0.9rem;
  }
  
  .paper-link:hover {
    text-decoration: underline;
  }

  .paper-authors {
    color: var(--global-text-color);
    font-size: 0.9rem;
    margin-bottom: 0.5rem;
  }

  .paper-authors strong {
    font-weight: bold;
  }
</style>


<!-- News -->
<div class="news mt-3 p-0">
  <h3 class="title mb-4 p-0">News</h3>
  {% for item in site.data.news limit: site.news_limit %}
    <div class="row p-0">
      <div class="col-sm-2 p-0">
        <span class="badge danger-color-dark darken-1 font-weight-bold text-uppercase align-middle date ml-3">
          {{ item.date | date: "%b %-d, %Y" }}
        </span>
      </div>
      <div class="col-sm-10 mt-2 mt-sm-0 ml-3 ml-md-0 p-0 font-weight-light text">
        <p>{{ item.content | emojify }}</p>
      </div>
    </div>
  {% endfor %}
</div>

<!-- Publications -->
<div class="publications mt-3 p-0">
  <h3 class="title mb-4 p-0">Publications</h3>

  <!-- Add the CSS -->
  <style>
    .tag-buttons {
      margin-bottom: 1.5rem;
    }
    .tag-button {
      display: inline-block;
      padding: 0.3rem 0.8rem;
      margin: 0.2rem;
      border-radius: 999px;
      font-size: 0.875rem;
      cursor: pointer;
      transition: all 0.2s;
      background-color: #f8f9fa;
      border: 1px solid #dee2e6;
    }
    .tag-button:hover {
      background-color: #e9ecef;
    }
    .tag-button.active {
      background-color: #1976d2;
      color: white;
      border-color: #1976d2;
    }
    .paper-item {
      display: flex;
      gap: 1.5rem;
      margin-bottom: 1.5rem;
      padding: 1rem;
      border-radius: 0.5rem;
      background-color: white;
      transition: all 0.2s;
      min-height: 160px;
    }
    .paper-item:hover {
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }
    .paper-image {
      width: 100%;
      height: 100%;
      object-fit: contain;
      border-radius: 0.375rem;
    }
    .paper-image-container {
      flex: 0 0 200px;  /* Fixed width, won't grow or shrink */
      height: 140px;    /* Fixed height */
      position: relative;
      overflow: hidden;
      border-radius: 0.375rem;
    }
    .paper-info {
      flex-grow: 1;
    }
    .paper-title {
      color: var(--global-theme-color);
      font-size: 1.1rem;
      font-weight: 500;
      text-decoration: none;
      margin-bottom: 0.5rem;
      display: block;
    }
    .paper-title:hover {
      text-decoration: underline;
    }
    .paper-authors {
      color: var(--global-text-color);
      font-size: 0.9rem;
      margin-bottom: 0.75rem;
    }
    .paper-tag {
      display: inline-block;
      padding: 0.2rem 0.6rem;
      margin: 0.2rem;
      border-radius: 999px;
      background-color: #f8f9fa;
      color: var(--global-text-color);
      font-size: 0.75rem;
    }
    @media screen and (max-width: 576px) {
      .paper-item {
        flex-direction: column;
        min-height: auto;
      }
      .paper-image {
        width: 100%;
        margin-bottom: 1rem
      }
    }
  </style>

  <!-- JavaScript for filtering -->
  <script>
    document.addEventListener('DOMContentLoaded', function() {
      const papers = document.querySelectorAll('.paper-item');
      const tagButtons = document.querySelectorAll('.tag-button');
      let activeFilters = new Set();

      tagButtons.forEach(button => {
        button.addEventListener('click', function() {
          const tag = this.getAttribute('data-tag');
          if (activeFilters.has(tag)) {
            activeFilters.delete(tag);
            this.classList.remove('active');
          } else {
            activeFilters.add(tag);
            this.classList.add('active');
          }
          filterPapers();
        });
      });

      function filterPapers() {
        if (activeFilters.size === 0) {
          papers.forEach(paper => paper.style.display = 'flex');
          return;
        }
        papers.forEach(paper => {
          const paperTags = Array.from(paper.querySelectorAll('.paper-tag'))
            .map(tag => tag.textContent.trim());
          const shouldShow = Array.from(activeFilters)
            .some(filter => paperTags.includes(filter));
          paper.style.display = shouldShow ? 'flex' : 'none';
        });
      }
    });
  </script>

  <!-- Filter buttons -->
  <div class="tag-buttons">
    {% assign all_tags = "" | split: ',' %}
    {% for paper in site.data.papers %}
      {% for tag in paper.tags %}
        {% assign all_tags = all_tags | push: tag %}
      {% endfor %}
    {% endfor %}
    {% assign unique_tags = all_tags | uniq | sort %}
    {% for tag in unique_tags %}
      <button class="tag-button" data-tag="{{ tag }}">{{ tag }}</button>
    {% endfor %}
  </div>

<!-- Papers list -->
{% for paper in site.data.papers %}
  <div class="paper-item">
    <div class="paper-image-container">
      <img src="{{ paper.image | relative_url }}" alt="{{ paper.title }}" class="paper-image">
    </div>
    <div class="paper-info">
      <a href="{{ paper.links.paper }}" class="paper-title" target="_blank" rel="noopener noreferrer">
        {{ paper.title }}
      </a>
      <div class="paper-authors">
        {% for author in paper.authors %}
          {% if author contains "Haofei Yu" %}
            <strong>{{ author }}</strong>
          {% else %}
            {{ author }}
          {% endif %}
          {% unless forloop.last %}, {% endunless %}
        {% endfor %}
      </div>
      <div class="venue">{{ paper.venue }}</div>
      <div class="paper-links">
        {% if paper.links.paper %}
          <a href="{{ paper.links.paper }}" target="_blank" rel="noopener noreferrer" class="paper-link">Paper</a>
        {% endif %}
        {% if paper.links.code %}
          <a href="{{ paper.links.code }}" target="_blank" rel="noopener noreferrer" class="paper-link">Code</a>
        {% endif %}
        {% if paper.links.data %}
          <a href="{{ paper.links.data }}" target="_blank" rel="noopener noreferrer" class="paper-link">Data</a>
        {% endif %}
        {% if paper.links.model %}
          <a href="{{ paper.links.model }}" target="_blank" rel="noopener noreferrer" class="paper-link">Model</a>
        {% endif %}
        {% if paper.links.media %}
          <a href="{{ paper.links.media }}" target="_blank" rel="noopener noreferrer" class="paper-link">Media</a>
        {% endif %}
      </div>
      <div class="paper-tags">
        {% for tag in paper.tags %}
          <span class="paper-tag">{{ tag }}</span>
        {% endfor %}
      </div>
    </div>
  </div>
{% endfor %}
</div>



<script type="text/javascript" id="clustrmaps" src="//cdn.clustrmaps.com/map_v2.js?cl=ffffff&w=700&t=tt&d=NhXj4joI7G-QcI07Qz4cPPkmnIj_bE-Zi4HhgEt-oCs"></script>
