---
title: Reference
permalink: /presentations/
---

# Lab meetings!

Every Monday at 9:00 a.m, we get together (mix of virtual and in person) for lab presentations (with food! sometimes).
On a rotating basis, each member of the lab speaks and teaches about something they know or shares their work. 
Anything, really. Relevant and interesting topics, good skills to know, nice Python packages,
neuroscientific princples, new findings and literature reviews... anything!

<div style="border-top: 2px dashed gray; width: 100%; margin: 20px 0;"></div>


### Spring 2024
{% raw %}
| Date | Name | Topic |
|------|------|-------|
| Sep 9 | --- | Lab Meeting |


<!-- 
| Jan 26 [Fri] | K-lab retreat | N/A |
| Feb 2 | Lab business | Discussion |
| Feb 9 |Joey R. | Conformal Prediction |
| Feb 16 | Alessandro Lamacchia | Servers! |
| Feb 23 | Reading club | Episodic Memory |
| Mar 1 | Lab 1-1s | do 'em |
| Mar 8 | Lab 1-1s | do 'em |
| Mar 15 | ... | ... |
| Mar 22 | Tony | "Modern" Causal Inference |
| Mar 29 | ... | ... |
| Apr 5 |Felipe P | sts experiments, tracking |
| Apr 12 | Joey | How to program a brain | -->

<!-- 
一月 January = Jan

二月 February = Feb

三月 March = Mar

四月 April = Apr

五月 May = May

六月 June = Jun

七月 July = Jul

八月 August = Aug

九月 September = Sep / Sept

十月 October = Oct

十一月 November = Nov

十二月 December = Dec -->



<!-- {% endraw %}

{% assign reference_types = "scientists|students" | split: "|" %}

{% for type in reference_types %}

{% if type == 'scientists' %}
### **For scientists**
 {% elsif type == 'students' %}
### **For students, lab members**
{% endif %}

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains type %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">- {{ post.title }}</a>
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>

<hr>
{% endfor %}

### **Older Blog posts from the lab**

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'blog' %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">- {{ post.title }}</a> (<small>{{post.date | date: "%m/%d/%y" }}</small>)
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>

<hr> -->

<div style="border-top: 2px dashed gray; width: 100%; margin: 20px 0;"></div>


<!-- 展示写的短文 -->
<h3> Blogs <h3>
<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'blog' %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">- {{ post.title }}</a> (<small>{{post.date | date: "%y/%m/%d" }}</small>)
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>