---
layout: page
title: Welcome To My Blog

---

{% include JB/analytics %}
<ul class="posts">
  {% for post in site.posts %}
      <li><span>{{ post.date | date_to_string }} <a href="{{ BASE_PATH }}{{ post.url }}" > <h2>{{ post.title }} </h2>
	  {{post.content| truncatehtml}}</a></span> 
	  </li>


  <p></p>
  <p></p>
  {% endfor %}
</ul>

