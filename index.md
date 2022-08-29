---
layout: home
title: Home
---
<div id ="intro-wrapper" class="l-middle">
	<div id="intro-title-wrapper" style="height: 0.5rem" class="intro-left">
		<h1 id="post-title">Home</h1>
	</div>
	<div class="intro-left">
		<div class="intro-left">
			Hello, my name is <b>Bryan Lu</b>. I am a master's student in the <u>machine learning</u> department at Carnegie Mellon University. I graduated from Vanderbilt University with majors in <u>mathematics</u> and <u>computer science</u>. 
		</div>
		<div style="height: 1rem"></div>
		<div class="intro-left">
			My research background lies in <u>machine learning</u>, <u>computer vision</u>, and <u>data visualization</u>. I am interested in making machine learning solugit tions more deployable. To me, this means designing geometrically aware algorithms and building novel interfaces to assist stakeholders audit trained models.
		</div>
		<div style="height: 1rem"></div>
		<div style="height: 1rem"></div>
		<div class="intro-left">
			As a first-generation student, I believe everyone deserves access to quality education, no matther their family background. I am a co-founder of <a href="http://mp.weixin.qq.com/mp/homepage?__biz=MzA4OTQ4NDA4MA==&hid=4&sn=75aefeab543f892090c68b70750530f5&scene=18#wechat_redirect">Gaokaopedia</a>. 
		</div>
	</div>
	<div class="intro-right">
		<img id="intro-image" class="intro-right" src="/images/portrait.jpg">
		<div style="height: 0.5rem"></div>
		<div id="intro-image-links" class="intro-right">
			{% for link in site.data.social-links %}
				{% if link.on-homepage == true %}
					{% include social-link.html link=link %}
				{% endif %}
			{% endfor %}
		</div>
		<div style="height: 0.5rem"></div>
		<div id="intro-cv-wrapper" class="intro-right">
			{% for link in site.data.social-links %}
				{% if link.id == "cv-web" %}
					{% include social-link.html link=link %}
				{% endif %}
			{% endfor %}

		</div>
	</div>
</div>



<hr class="l-middle home-hr">

<h2 class="feature-title l-middle">
	<!-- Selected <a href="/cv#publications">Publications</a> -->
	Selected <a href="https://scholar.google.com/citations?hl=en&user=R6bq6u4AAAAJ">Publications</a>
</h2>

<div class="l-middle">
	{% assign selectedBoolForBibtex = true %}
	{% for pub in site.data.pubs %}
		{% include publication.html pub=pub selectedBoolForBibtex=selectedBoolForBibtex %}
	{% endfor %}
</div>