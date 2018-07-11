---
title: Galline
tags: [special_layouts]
keywords: knowledge base, support portal, grid, doc portal
last_updated: July 3, 2016
summary: "This shows a sample layout for a knowledge base. Each square could link to a tag archive page. In this example, font icons from Font Awesome are used for the graphics, and the layout is pulled from the Modern Business theme. ."
sidebar: galline_sidebar
permalink: galline.html
toc: false
folder: galline
---

Here's the sample knowledge-base style layout:

<div class="row">
         <div class="col-lg-12">
             <h2 class="page-header">Basic Needs</h2>
         </div>
         <div class="col-md-3 col-sm-6">
             <div class="panel panel-default text-center">
                 <div class="panel-heading">
                     <span class="fa-stack fa-5x">
                           <i class="fa fa-circle fa-stack-2x text-primary"></i>
                           <i class="fa fa-tree fa-stack-1x fa-inverse"></i>
                     </span>
                 </div>
                 <div class="panel-body">
                     <h4>Water</h4>
                     <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
                     <a href="gal_clean_water.html" class="btn btn-primary">Learn More</a>
                 </div>
             </div>
         </div>
         <div class="col-md-3 col-sm-6">
             <div class="panel panel-default text-center">
                 <div class="panel-heading">
                     <span class="fa-stack fa-5x">
                           <i class="fa fa-circle fa-stack-2x text-primary"></i>
                           <i class="fa fa-car fa-stack-1x fa-inverse"></i>
                     </span>
                 </div>
                 <div class="panel-body">
                     <h4>Food</h4>
                     <p>All about food.</p>
                     <a href="tag_chickens_food.html" class="btn btn-primary">Learn More</a>
                 </div>
             </div>
         </div>
         <div class="col-md-3 col-sm-6">
             <div class="panel panel-default text-center">
                 <div class="panel-heading">
                     <span class="fa-stack fa-5x">
                           <i class="fa fa-circle fa-stack-2x text-primary"></i>
                           <i class="fa fa-support fa-stack-1x fa-inverse"></i>
                     </span>
                 </div>
                 <div class="panel-body">
                     <h4>Housing</h4>
                     <p>All about how to build a shelther for your chickens.</p>
                     <a href="tag_chicken_housing.html" class="btn btn-primary">Learn More</a>
                 </div>
             </div>
         </div>
         <div class="col-md-3 col-sm-6">
             <div class="panel panel-default text-center">
                 <div class="panel-heading">
                     <span class="fa-stack fa-5x">
                           <i class="fa fa-circle fa-stack-2x text-primary"></i>
                           <i class="fa fa-database fa-stack-1x fa-inverse"></i>
                     </span>
                 </div>
                 <div class="panel-body">
                     <h4>Formatting</h4>
                     <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
                     <a href="tag_formatting.html" class="btn btn-primary">Learn More</a>
                 </div>
             </div>
         </div>
</div>


Tutte le pagine:

<ul>
{% assign sorted_pages = site.pages | sort: 'title' %}
{% for page in sorted_pages %}
{% for tag in page.tags %}
{% if tag == "chicken" %}
<li><a href="{{ page.url | remove: "/"}}">{{page.title}}</a></li>
{% endif %}
{% endfor %}
{% endfor %}
</ul>

{% include links.html %}
