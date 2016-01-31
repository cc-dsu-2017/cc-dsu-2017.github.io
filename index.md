---
layout: default
title: Home
---

# Cloud Computing @ Dayananda Sagar University, 2015

## Projects

{% for repository in site.github.public_repositories %}
 * {{ repository.title }} [{{ repository.name }}]({{ repository.html_url }})

{% endfor %}

## Members

{% for member in site.github.organization_members %}
  * ![]({{ member.avatar_url}}) {% include icon-github.html username=member.login %}
{% endfor %}

## Posts

{% for post in site.posts %}
  * {{ post.date | date: "%b %-d, %Y" }} [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
{% endfor %}

Subscribe [via RSS]("{{ "/feed.xml" | prepend: site.baseurl }})
