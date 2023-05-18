---
layout: full_page
title: about
permalink: /
# subtitle: <a href='#'>Affiliations</a>. Address. Contacts. Moto. Etc.
# subtitle: Computer Vision | Machine Learning

# profile:
#   align: right
#   image: prof_pic.jpg
#   address: >
#     <p>555 your office number</p>
#     <p>123 your address street</p>
#     <p>Your City, State 12345</p>
profile:
  align: 
  image: 
  address: 

news: false  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page
display_categories: [projects, teaching, other]
---

I am a graduating MS student in the Computer Science Department at Cornell University, studying and performing research in Machine Learning and Computer Vision. I am proud to be advised by <a href='https://www.cs.cornell.edu/~bharathh/'>Bharath Hariharan</a> and <a href='https://web.stanford.edu/~udell/'>Madeleine Udell</a>. Prior to my MS, I completed my Bachelor of Science degree in Computer Science from Cornell University, specializing in Machine Learning and Computer Vision.

My research and engineering interests lie broadly in understanding, developing, and applying deep learning methods for computer vision and machine learning. Some research areas that I have been involved in throughout my graduate and undergraduate years are representation/self-supervised learning, data augmentation, deep generative models, missing data, amodal/panoptic image segmentation, 3D object detection and tracking, and parallel + distributed machine learning.

I am also proud of being a teaching assistant at the Computer Science Department at Cornell University for over three years. Teaching seven machine learning + computer vision upper-division and graduate semester-long courses.

Currently, I am looking for machine learning (research) engineer opportunities!

**Contact:** rgh224 [at] cornell.edu

<style>
.col-sm-7{

}

.course {
margin: 0;
padding: 0;
}

.institution {
margin: 0;
padding: 0.2em;
font-style: italic;
}
</style>

<div class="row">    
  <div class="col-sm-5">
      <h3>Interests</h3>
      <ul class="ul-interests">  
        <li>Machine Learning and Computer Vision</li> 
        <li>Science of Deep Learning</li> 
        <li>Self- and Semi-Supervised Learning</li> 
        <li>Deep Generative Models</li>
        <li>Data Augmentation</li>
        <li>Object Detection, Tracking, and Segmentation</li>
        <li>Distributed Machine Learning</li>
      </ul>
    </div>     
  <div class="col-sm-7">
    <h3>Education</h3>
    <ul class="ul-edu fa-ul">
      <li>
        <i class="fa-li fa fa-graduation-cap"></i>
        <div class="description">
          <p class="course"> <b>MS in Computer Science</b>, Expected 2023  </p>
          <p class="institution">Cornell University</p>
        </div>
        <i class="fa-li fa fa-graduation-cap"></i>
        <div class="description">          
          <p class="course"> <b>BS in Computer Science</b>, 2020 </p>
          <p class="institution">Cornell University</p>
        </div>
      </li>
    </ul>
  </div>
</div>

<!-- 
The main areas that I have be involved in are the following:
* Representation/Self-Supervised learning 
* Data augmentation with generative models
* Missing data
* Amodal/Panoptic Segmentation
* Parallel and distributed machine learning
 -->


<!-- Put your address / P.O. box / other info right below your picture. You can also disable any these elements by editing `profile` property of the YAML header of your `_pages/about.md`. Edit `_bibliography/papers.bib` and Jekyll will render your [publications page](/al-folio/publications/) automatically.

Link to your social media connections, too. This theme is set up to use [Font Awesome icons](http://fortawesome.github.io/Font-Awesome/) and [Academicons](https://jpswalsh.github.io/academicons/), like the ones below. Add your Facebook, Twitter, LinkedIn, Google Scholar, or just disable all of them. -->

<!-- ---
layout: page
title: projects
# description: A growing collection of your cool projects.
nav: true
nav_order: 3
# display_categories: [preprints, extra]
horizontal: false
--- -->

<!-- page.html -->
       
<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %} 
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category" id={{ category }}>{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}
{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>