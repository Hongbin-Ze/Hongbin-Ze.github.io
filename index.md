---
layout: page
title: "Home"
class: home
---

<h1> Hi, I'm Hongbin Na </h1>

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm an a second-year Master of Research student in [Australian AI Institute](https://www.uts.edu.au/research/australian-artificial-intelligence-institute) at  [University of Technology Sydney](https://www.uts.edu.au/), affiliated with the [UTS NLP Group](https://utsnlp.github.io/), where I am advised by [Ling Chen](https://profiles.uts.edu.au/Ling.Chen) (UTS), supervised by [Tao Shen](https://scholar.google.com/citations?user=SegyX9AAAAAJ&hl=en) (Oracle) and work closely with [Yining Hua](https://ningkko.github.io/), [John Torous](https://corporatelearning.hms.harvard.edu/faculty-staff/john-torous) (Harvard) and [Shaoxiong Ji](https://shaoxiongji.github.io/) (TU Darmstadt).

My research interests focus on the field of Natural Language Processing (NLP), specifically in dialogue systems and mental health. My goal is to combine psychology with large language models (LLMs) to explore and develop models capable of understanding complex human emotions and cognitive processes. 

I’m always open to collaborating with graduate/undergraduate students, particularly for **beginners** and **the underrepresented**. Feel free to email me if you’d like to connect or have a virtual coffee chat! 😊

</div>

<div class="me" markdown="1">
<picture>
  <!-- <source srcset='/images/dominik_berlin.webp' type='image/webp' /> -->
  <img
    src='images/profile.png'
    alt='Hongbin Na'
    style='max-width: 100%; height: auto;'>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
</div>


</div>

<div class="news-travel" markdown="1">

<div class="news" markdown="1">
## News

<ul>
{% for news in site.data.news limit:10 %}
  {% include news.html news=news %}
{% endfor %}
</ul>

</div>

<div class="travel" markdown="1">
## Travel

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

</div>

</div>

<div class="quote-section" markdown="1">
> "Let's beat these illnesses with research, but also by creating a world in which nobody feels reluctant to talk openly."
> 
> *— Felix Hill*
</div>

