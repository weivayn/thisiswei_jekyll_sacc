---
layout: post
title: Jekyll Tags
tags:
- Jekyll
- Code
---

Thanks to [Charlie Park](https://github.com/charliepark/charliepark.github.com){:target="`_blank`"}'s tutorial on how to add [Tags In Jekyll](http://charliepark.org/tags-in-jekyll/){:target="`_blank`"}! I was able to add tags into my blog posts.

There was an additional step that I took to make tags to be fully functional, which was to included **{{ site.baseurl }}** tag in front of the **/tag/{{ tag }}**, where I had hyperlinks or **href**.
    ```
      <ul class="tag_list_in_post">
        {% for tag in page.tags %}
        <li class="inline tag_list_item">
          <a class="tag_list_link" href="**{{ site.baseurl }}**/tag/{{ tag }}">{{ tag }}</a>
        </li>
        {% endfor %}
      </ul>

Now, it's time to style them!
