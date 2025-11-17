---
layout: page
title: "Home"
class: home
---

# Hi, I'm Namrata Mukhija

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm currently an Applied Scientist at Amazon in the Sponsored Products team where I work with LLM Agents for designing thematic recommendations shown on Amazon.com's Search page. I was previously an Applied Scientist at JPMorgan Chase and Co. working in the [Machine Learning Center of Excellence](https://www.jpmorgan.com/technology/applied-ai-and-ml/machine-learning) on developing RAG agents. Outside of my full-time job, I'm an active contributor at EAAMO Bridges [Living Labs with Practioners](https://bridges.eaamo.org/working_groups/conversations-with-practitioners/) group aimed at co-experimentation and implementing participatory methodology with social impact practitioners and nonprofits. I graduated with a M.S. in Computer Science from [New York University, Courant School of Mathematical Sciences](https://www.courant.nyu.edu/).
  
Previously, I've researched on assessing stereotype detection capability in large language models during a fellowship at [Arthur AI](https://www.arthur.ai/) under [Dr. John Dickerson](https://www.linkedin.com/in/john-dickerson). I've also researched into paraphrasing as a data augmentation tool in improving Named Entity Recognition task performance in low versus high resource scenarios (ACL'23 and NeurIPS'22) during my internship at [J.P. Morgan, Machine Learning Center of Excellence](https://www.jpmorgan.com/technology/applied-ai-and-ml). During my internship at Microsoft Research, India under [Dr. Kalika Bali](https://www.microsoft.com/en-us/research/people/kalikab/) and [Dr. Monojit Choudhury](https://www.microsoft.com/en-us/research/people/monojitc/), I worked on developing a [framework](https://arxiv.org/abs/2110.07444) for prioritizing research for low-resource language communities, understanding different dilemmas [(ACM COMPASS'25](https://dl.acm.org/doi/10.1145/3530190.3534792) faced by technologists, their origin and complexity, and involving low-resource language communities in the development of language technologies. 
  
Before my Masters, I was a Software Engineer 2 at [Microsoft](https://www.microsoft.com/). I was involved in developing various products such as [PowerPoint](https://www.microsoft.com/en-in/microsoft-365/powerpoint), [Fluid Framework](https://fluidframework.com/), and [Unified Service Desk](https://docs.microsoft.com/en-us/dynamics365/unified-service-desk/admin/overview-unified-service-desk?view=dynamics-usd-4.1).

I received my B.E. in Information Technology from [Netaji Subhas University of Technology](http://www.nsit.ac.in/).

I was awarded the Microsoft Experiences+Devices India Leadership Award 2020 across 2500+ employees for generating energy in the team, demonstrating ”All for One, One for All” mindset, and championing diversity and inclusion.

I actively work and volunteer for non-profits working towards closing the gender gap across industries - [Women in AI](http://www.womeninai.co/) where I used to lead the Women in AI India chapter and a contributor at EAAMO Bridges [Living Labs with Practioners] (https://bridges.eaamo.org/working_groups/conversations-with-practitioners/) group. If you have an idea that could help reduce the gender gap, please <a href="mailto:namrata@womeninai.co">reach out</a> to me!
</div>

<div class="me" markdown="1">
<picture>
  <img
    src='/images/namrata.jpg'
    alt='Namrata Mukhija'/>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
</div>

</div>

## Featured Projects

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>
<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Projects
</a>

<!-- ## Featured Publications -->

<!-- <div class="featured-publications">
  {% for pub in site.publications %}
    {% if pub.highlight %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{{ pub.venue }}, {{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a>

<div class="news-travel" markdown="1">

<div class="news" markdown="1">
## Latest News

<ul>
{% for news in site.data.news limit:10 %}
  {% include news.html news=news %}
{% endfor %}
</ul>

</div>

<div class="travel" markdown="1">
## Latest Travel

<table>
<tbody>
{% assign future_travel = site.data.travel | where_exp:'item','item.start == null' %}
{% for travel in future_travel %}
  {% include travel.html travel=travel %}
{% endfor %}
{% assign sorted_travel = site.data.travel | where_exp:'item','item.start' | sort: 'start' | reverse %}
{% for travel in sorted_travel limit:10 %}
  {% include travel.html travel=travel %}
{% endfor %}
</tbody>
</table>

</div> -->

<!-- </div> -->
