---
title: Conference program
---

<div class="keynote-full">

{% if site.data.conference[0].name %}
	{% assign speakers = site.data.conference | sort: 'time' %}
	<table>
	{% for speaker in speakers %}
	  <tr>
	    <td>{{speaker.time}}</td>
	    <td>{{speaker.name}}</td>
	    <td><a href="/program/conference#{{speaker.name | replace: " ","-"}}">{{speaker.title}}</a></td>
	  </tr>
	{% endfor %}
	</table>
{% else %}
  <p><br>
     We're currently in the progress of making the conference program.<br>
     We will share the information very soon.
  </p>
{% endif %}
</div>
