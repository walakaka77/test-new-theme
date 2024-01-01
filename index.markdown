---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

# Home Page

This site is using the Jekyll Theme Hacker page look.

Here is the list of available posts so far:

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


And these are the list of pages for your review:
<ul>
  {% assign baseurl = site.baseurl %}
  {% for page in site.pages %}
    {% if page.url contains 'about' or page.url contains 'second-category' %}
      <li>
        <a href="{{ baseurl | append: page.url }}">{{ indentation }}{{ page.title }}</a>
        <!-- <a href="{{ baseurl }}">{{ indentation }}{{ page.title }}</a> -->
      </li>
    {% endif %}
  {% endfor %}
</ul>