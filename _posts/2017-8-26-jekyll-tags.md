---
layout: post
title: Jekyll Tags
tags:
- Jekyll
- Code
---

Thanks to [Charlie Park](https://github.com/charliepark/charliepark.github.com)'s tutorial on how to add [Tags In Jekyll](http://charliepark.org/tags-in-jekyll/)! I was able to add tags into my blog posts.

The two additional things that I did to make the tags were fully functional were:

1. Added the following configuration in the **_config.yml** file for letting Jekyll know which plugins should be used in my site.
    ```
      plugins:
        - tag_gen
    ```
2. Included **{{ site.baseurl }}** tag in front of the **/tag/{{ tag }}**, where I had hyperlinks or **href**.
    ```
      <ul class="tag_list_in_post">
        {% for tag in page.tags %}
        <li class="inline tag_list_item">
          <a class="tag_list_link" href="**{{ site.baseurl }}**/tag/{{ tag }}">{{ tag }}</a>
        </li>
        {% endfor %}
      </ul>
    ```

Now, it's time to style them!
