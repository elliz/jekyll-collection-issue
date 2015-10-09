---
title: "Demo for possible issue on Jekyll Collections"
description: this site demonstrates a possible issue with Jekyll collections

layout: default
---

## Items collection

If there is an issue then only one item should show up below. 
If there is no issue then there will be two items:

{% for item in site.items %}
  * [{{ item.title }}]({{ site.baseurl }}{{ item.url }})
{% endfor %}

## Posts

Posts are created from identical files to the Items collection (literally copy and paste then add timestamp to filename).
There should be two files listed below:

{% for item in site.posts %}
  * [{{ item.title }}]({{ site.baseurl }}{{ item.url }})
{% endfor %}