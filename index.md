---
layout: default
---

## About Me

<img class="profile-picture" src="/image/WechatIMG99.jpeg">

我们的生活可能都是看似平淡的，看似困顿无聊的，可是里面饱含着不为人知的神秘的随机性，那种大命运之上有着各种各样让人目眩神迷的小机关。

流水不争先，争的是滔滔不绝。

---

<div>
  {% for post in site.posts %}
    <div class="blog-list" style="margin-bottom:50px;">
      <blockquote>
        <p>{{ post.date | date: '%B %d, %Y' }} <a href="{{ post.url }}">>>></a></p>
        <p>{{ post.description }}</p>
      </blockquote>
      <!-- <a href="{{ post.url }}">{{ post.title }}</a> -->
      <!-- <p>{{ post.description }}</p> -->
       {% if post.images_show == 1 %}
           <div class="card-columns">
       {% endif %}
        {% if post.images_show == 2 %}
         <div class="">
       {% endif %}
       {% for img in post.images %}
            <div class="card" data-toggle="modal" data-target="#exampleModal" data-img="{{ img }}">
                <img class="lozad card-img-top" data-src="{{ img }}" />
            </div>
       {% endfor %}
      </div>
    </div>
  {% endfor %}
</div>