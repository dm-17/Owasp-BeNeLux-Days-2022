---
title: Social event
---

<div class="social-event">

  <p><br>
  On Thursday evening we organize a social event in <a href="https://www.agora-tilburg.nl/">Agora Tilburg</a>.<br>
You are welcome to join us for a dinner as of 18:30.<br><br>
Please <a href="https://owasp-benelux-days-fall-2022.eventbrite.com/">register</a> when you plan to come?
The social event is free, but everyone pays for themself.<br />
There is limited space available in Agora Tilburg. The social event is first come first serve.


  </p>

{% assign socialEventSponsors = site.data.sponsors | where:"level","Social event" | sort: 'name' %}

  {% if socialEventSponsors %}
    {% for sponsor in socialEventSponsors %}
      <div class="socialevensponsor">
        <a href="{{ sponsor.url }}"><img src="/assets/images/sponsors/{{ sponsor.image }}" alt="{{ sponsor.name }} logo" style="{{ sponsor.style }}"/></a><br />
      </div>
    {% endfor %}
  {% endif %}

</div>
