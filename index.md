---
title: "Demo for possible issue on Jekyll Collections"
description: this site demonstrates a possible issue with Jekyll collections

layout: default
---

This is a demo page to demonstrate [Jekyll issue 4017](https://github.com/jekyll/jekyll/issues/4017)

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

## XML Tests

* [XML without space after first ---](without-space.xml)
* [XML with space after first ---](with-space.xml) - will show as error - not valid xml