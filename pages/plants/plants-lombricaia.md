---
title: Catalogo Piante Feeds
tags: [plants]
keywords:
last_updated: July 10, 2018
summary: ""
sidebar: plants_sidebar
permalink: plants-lombricaia
toc: true
---

<div class="lista-short">
	<div class="container">
		<div class="plants">

			<input id="search-highlight" class="mb-4" name="search-highlight" placeholder="Cerca una pianta" type="text" data-list=".highlight_list" autocomplete="on">
	            <div class="vertical highlight_list">
	            	
	            	{% assign plants = site.data.plants | sort: 'nome_principale' %}
	              	{% for p in plants %}
	              		{% if p.luoghi contains "lombricaia" %}
					  		{% include plant-short-card.html %}
						{% endif %}
						
					{% endfor %}
	        	</div>
	    </div>
	
	</div>
</div>
 <!-- JS -->
<!-- JS ends -->