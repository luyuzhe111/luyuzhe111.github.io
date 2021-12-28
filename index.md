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
			Hello, my name is <b>Yuzhe Lu</b>. I am a senior at Vanderbilt University with majors in <u>mathematics</u> and <u>computer science</u>. 
			<!-- and minors in <u>data science</u> and <u>medicine, health, and society</u>.  -->
			<!-- I have been privileged do research with amazing faculties here at Vanderbilt: <a href="https://engineering.vanderbilt.edu/bio/yuankai-huo">Dr. Yuankai Huo</a>, <a href="https://engineering.vanderbilt.edu/bio/bennett-landman">Dr. Bennett Landman</a>, <a href="https://matthewberger.github.io/">Dr. Matthew Berger</a>, and <a href="https://skolouri.github.io/">Dr. Soheil Kolouri</a>. -->
		</div>
		<div style="height: 1rem"></div>
		<div class="intro-left">
			My research interest lies at the intersection of <u>machine learning</u>, <u>computer vision</u>, and <u>human-computer interaction</u>. In particular, I am interested in <u>making representation learning in computer vision more tangible</u>. To this end, I have worked on <u>interactive interfaces</u> to characterize model representations and <u>novel frameworks</u> to improve learning outcomes.
			<!-- I am interested in <b>data visualization</b>, <b>medical image computing</b>, and <b>machine learning</b>. My goal is to develop <u>visually or theoretically interpretable machine intelligence, especially for biomedical applications</u>. This involves utilizing data visualization techniques to understand learned representations and guild model development, and leveraging mathematical lens to build theoretically-grounded frameworks.    -->
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