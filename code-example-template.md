# Title

## Description
	If useful, include links to objects.properties in docs in the description (this snippet uses
	product.collections and product.images)

## Instructions:
 - steps/instructions
 - dependencies
 - variants
 - warnings
 - exceptions

## Tags
(fake labels = link to the filtered search)

## Date (last updated)

## Component code

```liquid
<div class="comment__content rte">
  {{ comment.content }}
</div>
<div class="comment__meta">
  {% capture author %}<strong>{{ comment.author }}</strong>{% endcapture %}
  {% capture date %}<strong><time datetime="{{ comment.created_at | date: '%Y-%m-%d' }}">{{ comment.created_at | date: format: 'month_day_year' }}</time></strong>{% endcapture %}
  {{ 'blogs.article.comment_meta_html' | t: author: author, date: date }}
</div>

```
