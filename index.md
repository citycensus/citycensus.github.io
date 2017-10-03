---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
---
{% include banner.html %}
  <!-- Section -->
<section>
	<div class="features">
		{% for feature in site.data.features %}
			<article>
				<span class="icon {{feature.icon}}"></span>
				<div class="content">
					<h3>{{feature.title}}</h3>
					<p>{{feature.text | markdownify}}</p>
				</div>
			</article>
		{% endfor %}
	</div>
</section>

<!-- Section -->
<section>
	<header class="major">
		<h2>News</h2>
	</header>
	<div class="posts">
		{% for post in site.posts %}
		<article>
			{% if post.image %}
        <a href="#" class="image"><img src="{{ post.image | prepend: '/assets/images/' | prepend: site.baseurl | absolute_url }}" alt="" /></a>
			{% endif %}
			<h3>{{post.title}}</h3>
			<p></p>
			<ul class="actions">
				<li><a href="{{post.url}}" class="button">More</a></li>
			</ul>
		</article>
		{% endfor %}
	</div>
</section>
