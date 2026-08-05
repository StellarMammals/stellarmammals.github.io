---
layout: page
permalink: /music/
title: Listen
description: Stream Stellar Mammals everywhere. Every release in one place, plus links to all platforms.
---
<div class="row justify-content-center">
	<div class="col-lg-9 text-center">
		<h2 class="section-heading text-uppercase">Listen</h2>
		<h3 class="section-subheading text-muted">Stream Stellar Mammals everywhere. Music for energy, dance, focus, and chill.</h3>

		<ul class="list-inline" style="margin:1.25rem 0 1.5rem">
			{% for link in site.data.navigation.en.streaming_links %}
			<li class="list-inline-item" style="margin:0.4rem 0.6rem">
				<a class="btn btn-primary" href="{{ link.url }}" target="_blank" rel="noopener">{% if link.icon %}<i class="{{ link.icon }}"></i> {% endif %}{{ link.name }}</a>
			</li>
			{% endfor %}
		</ul>
		<p class="text-muted">Buy and support on Bandcamp: <em>coming soon</em>.</p>

		<p style="margin-top:1.25rem">
			Browse by vibe:
			<a href="{{ '/house-and-horns/' | relative_url }}">House &amp; Horns</a> ·
			<a href="{{ '/lofi/' | relative_url }}">Lofi</a> ·
			<a href="{{ '/ambient/' | relative_url }}">Ambient</a>
		</p>
	</div>
</div>

<div class="row justify-content-center" style="margin-top:1.5rem">
	<div class="col-lg-10 text-center">
		<h3 class="section-heading text-uppercase">The Full Catalog</h3>
		<h4 class="section-subheading text-muted">Every Stellar Mammals release in one place.</h4>
	</div>
</div>

<div class="row">
	{% for item in site.portfolio %}
	<div class="col-md-6 col-lg-4 text-center" style="margin-bottom:2.25rem">
		<img src="{{ item.image | relative_url }}" alt="{{ item.alt }}" style="width:100%;max-width:260px;border-radius:8px">
		<h5 style="margin-top:0.8rem">{{ item.caption.title | default: item.title }}</h5>
		<div class="text-muted" style="font-size:0.9rem">{{ item.content }}</div>
	</div>
	{% endfor %}
</div>

<div class="row justify-content-center" style="margin-top:1rem">
	<div class="col-lg-9 text-center">
		<p><a class="btn btn-primary" href="#signup">Hear new releases first</a></p>
	</div>
</div>
