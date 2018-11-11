--
layout: page
title: Photos
images:
  - image_path: Crew-2018-Deathrow.jpeg
    title: Deathrow 2018
    desc: Deathrow 2018 (fifth from left)<br>Credit: Kristi Schlagen-Lindquist 
  - image_path: Crew-2018-SS-4.jpeg
    title: Sag Sprints 2018 - Four
    desc: Sag Sprints 2018 (right)<br>Credit: [Jillian Schulz](https://www.instagram.com/jillian_schulz_/)
  - image_path: Crew-2018-SS-2.jpeg
    title: Sag Sprints 2018 - Double
    desc: Sag Sprints 2018 (left)<br>Credit: [Jillian Schulz](https://www.instagram.com/jillian_schulz_/)
  - image_path: Crew-2018-HOM.jpeg
    title: Head of the Mississippi 2018
    desc: Head of the Mississippi 2018 (third from the right)<br>Credit: [Jillian Schulz](https://www.instagram.com/jillian_schulz_/)
  - image_path: Crew-2018-Northstar-race.jpeg
    title: Northstar 2018
    desc: Northstar 2018 (right)
  - image_path: Crew-2018-Northstar-boatpic.jpeg
    title: Northstar 2018
    desc: Northstar 2018 (right)
--


{% for image in page.images %}
  <div style="float: center; margin: 5px; width: 600px">
    <img src="{{  image.image_path }}" alt="{{ image.title }}" width="100%" height="auto">
    <div>{{ image.desc }}</div>
  </div>
{% endfor %}
