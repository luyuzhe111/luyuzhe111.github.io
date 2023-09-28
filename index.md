---
layout: home
title: home
---
<div id ="intro-wrapper" class="l-middle">
	<div id="intro-title-wrapper" style="height: 0.5rem" class="intro-left">
		<h1 id="post-title">Hello</h1>
	</div>
	<div class="intro-left">
		<div class="intro-left">
			My name is <b>Bryan Lu</b>. I am a master's student in the <u>machine learning</u> department at Carnegie Mellon University, working with <a href="https://www.ri.cmu.edu/ri-faculty/katia-sycara/">Katia Sycara</a>. Previously, I graduated from Vanderbilt University with honors in <u>computer science</u> and <u>mathematics</u>. I interned at <a href="https://aws.amazon.com/bedrock/titan/">AWS Titan Labs</a> and <a href="https://computing.llnl.gov/casc/machine-intelligence-group">LLNL Machine Intelligence Group</a>. 
		</div>
		<div style="height: 1rem"></div>
		<div class="intro-left">
			I have a diverse background in machine learning. Starting my research journey from deep learning applications in medical imaging & data visualization, I was deeply intrigued by the capability of these neural machinaries. Since then, I have been exploring tools / theories to systematically understand them. Ultimately, I want to build safe and responsible technologies. 
		</div>
		<div style="height: 1rem"></div>
		<div class="intro-left">
			As a first-generation student, I believe everyone should have access to quality education and dare to grow, no matther their background. I co-founded <a href="http://mp.weixin.qq.com/mp/homepage?__biz=MzA4OTQ4NDA4MA==&hid=4&sn=75aefeab543f892090c68b70750530f5&scene=18#wechat_redirect">Gaokaopedia</a>. I am currently part of <u>AI Mentoring for Underrepresented Student Groups</u> at CMU. 
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