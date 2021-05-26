---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Ruby Conf Taiwan 2021
layout: home
---

<div class='pb-5 text-center block-title brown-text'>News</div>
<div class='mb-5 d-flex flex-column' style='border-bottom: solid 1px #730000;'>
{% for each in site.data.news %}
  <div class='news-block p-4 d-flex row'>
    <div class='col-2'>{{each.time}}</div>
    <div class='col-10'>{{each.title}}</div>
  </div>
{% endfor %}
</div>

<div class='p-5 text-center block-title brown-text'>Speakers</div>
<div class='d-flex row'>
{% for each in site.data.speakers %}
  <div class='col-4 text-center speaker-box d-flex flex-column justify-content-center align-items-center'>
    <img src="{{each.avatar}}" height='200' width='200'/>
    <div class='mt-3'>{{each.name}}</div>
  </div>
{% endfor %}
</div>

<div class='px-7 pb-5 mt-5'>
  <div class='p-5 text-center block-title brown-text'>Schedule</div>
  <div class='news-block p-4 d-flex row brown-text text-center'>
    <div class='col-2 text-center'>Start</div>
    <div class='col-2 text-center'>End</div>
    <div class='col-8 text-center'>Title</div>
  </div>
  <div class='news-block p-4 d-flex row align-items-center news-content'>
    <div class='col-2 text-center'>Start</div>
    <div class='col-2 text-center'>End</div>
    <div class='col-8 text-center'>     
      <div class='talk-title'>Prime Section @ BR105</div>
      <div style='margin-top:10px'>Yukihiro Matsumoto (Matz)</div>
    </div>
  </div>
  <div class='d-flex justify-content-center row news-block p-4 brown-text text-center talk-day'>
      Day 1
  </div>
{% for each in site.data.schedule %}
  {% if each.day == 1 %}
    {% if each.title_main %}
      <div class='news-block p-4 d-flex row align-items-center news-content'>
        <div class='col-2 text-center'>{{each.time}}</div>
        <div class='col-2 text-center'>{{each.end}}</div>
        <div class='col-8 text-center'>     
          <div class='talk-title'>{{each.title_main}}</div>
          <div style='margin-top:10px'>{{each.speaker}}</div>
        </div>
      </div>
    {% else %}
      <div class='news-block p-4 d-flex row align-items-center schedule-break'>
        <div class='col-2 text-center'>{{each.time}}</div>
        <div class='col-2 text-center'>{{each.end}}</div>
        <div class='col-8 text-center'>
          <div class='talk-title'>{{each.title}}</div>
        </div>
      </div>
  {% endif %}
  {% endif %}
{% endfor %}
    <div class='d-flex justify-content-center row news-block p-4 brown-text text-center talk-day'>
      Day 2
    </div>
{% for each in site.data.schedule %}
  {% if each.day == 2 %}
    {% if each.title_main %}
    <div class='news-block p-4 d-flex row align-items-center news-content'>
      <div class='col-2 text-center'>{{each.time}}</div>
      <div class='col-2 text-center'>{{each.end}}</div>
      <div class='col-8 text-center'>
        <div class='talk-title'>{{each.title_main}}</div>
        <div style='margin-top:10px'>{{each.speaker}}</div>
      </div>
    </div>
  {% else %}
    <div class='news-block p-4 d-flex row align-items-center schedule-break'>
      <div class='col-2 text-center'>{{each.time}}</div>
      <div class='col-2 text-center'>{{each.end}}</div>
      <div class='col-8 text-center'>
        <div class='talk-title'>{{each.title}}</div>
      </div>
    </div>
  {% endif %}
  {% endif %}
{% endfor %}

<div class='p-5 text-center block-title brown-text'>Venue</div>
<div class='d-flex row align-items-center'>
  <div class='col-6'><img src='https://upload.wikimedia.org/wikipedia/commons/7/73/%E5%9C%8B%E7%AB%8B%E5%8F%B0%E7%81%A3%E7%A7%91%E6%8A%80%E5%A4%A7%E5%AD%B8%E7%A0%94%E6%8F%9A%E5%A4%A7%E6%A8%93.JPG' width='100%'/></div>
  <div class='col-6'>
    <div class='brown-text venue-text'>TR 214 AAEON Building, NTUST</div>
    <div style='color: #730000;font-size:18px; font-weight:400;'>研揚大樓 TR 214</div>
    <div class='my-3 addr'>
      <div>No. 43, Sec. 4, Keelung Rd., Da’an Dist., Taipei City</div>
      <div>106台北市大安區基隆路四段43號</div>
    </div>
    <a href="https://goo.gl/maps/vDHfM1o7KbsmxvbG6" target="_blank"><button class="btn btn-primary" type="button">Google Map</button></a>
  </div>
</div>

</div>
<div class='p-5 text-center block-title brown-text'>Sponsors</div>
<div class='sponsors text-center' style='margin-bottom:6rem!important;'>We are calling for sponsors, please contact sponsorship@coscup.org</div>