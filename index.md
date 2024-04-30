---
layout: home
indexmd: indexmd
---
{% comment %} - page

    {% for apage in page %}
      {{ apage }} = {{page[apage]|truncate 11}}
    {% endfor %} {% endcomment %}

- site
{% comment %} 遍历的元素为什么只是key不是键值对？？ {% endcomment %}
{% for asite in site %}
  {{ asite }} = {{site[asite]|truncate 11}}
{% endfor %}
{% comment %} page是键值对数组，遍历的元素是键值对，键值对是两个元素的数组，字典是个二维数组 {% endcomment %}
{% comment %} [[key, value], [key, value]] {% endcomment %}