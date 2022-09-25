---
title: Conference program
---

<div class="keynote-full">

{% if site.data.conference[0].name %}
	<h1>Confirmed speakers for Friday the 1st of April:</h1>
	<br />
	<ul>
	{% assign speakers = site.data.conference | sort: 'time' %}
	{% for speaker in speakers %}
		{% if speaker.name %}
		<li>
        <a name="{{speaker.name | replace: " ","-"}}">
        <img style="background-image: url(/assets/images/conference/{{speaker.image | default:'owasp_logo.png'}});{{speaker.style}};"></a>
      {% if speaker.title %}
        <h2>{{speaker.title}} by {{speaker.name}}</h2>
      {% else %}
        <h2>{{speaker.name}}</h2>
      {% endif %}

      <p><em>{{speaker.time}}</em>
      {% if speaker.feed %}
          - <a href="/program/feeds#{{speaker.name}}">Check out the streaming feed!</a>
      {% endif %}
      </p>

      {% if speaker.abstract %}
        <h4>Abstract:</h4>
          <p>{{speaker.abstract}}</p>
          <br>
      {% endif %}
      {% if speaker.bio %}
        <h4>Bio:</h4>
	<p>{{speaker.bio}}</p>
        <br>
      {% endif %}
		</li>
		{% endif %}
	{% endfor %}
	</ul>
{% else %}
  <p><br>
     We're currently in the progress of making the conference program.<br>
     We will share the information very soon.
  </p>
{% endif %}
</div>
