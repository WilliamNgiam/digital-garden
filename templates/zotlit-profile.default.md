---
id: default
name: Default
version: 1.0.0
author: ZotLit
description: The built-in format for literature notes.
contract: 3
filename: |
  {{ zt.citationKey | default: zt.DOI | default: zt.title | default: zt.key }}{% suffix %}
language: liquid
frontmatter:
  - key: title
    expr: zt.title
    merge: replace
  - key: author(s)
    expr: 'zt.authorsShort'
  - key: paper_doi
    expr: 'zt.DOI'
  - key: journal
    expr: zt.publicationTitle
  - key: citekey
    expr: zt.citationKey
    merge: replace
  - key: concept(s)
    value: ""
  - key: project(s)
    value: ""
  - key: aliases
    expr: zt.citekey
---


## Paper Annotations

{% for annotation in zt.annotations %}
{% render_annotation annotation %}
{% endfor %}



--- zotlit:annotation ---
{% bq %}
[!note]

{{ zt.imgLink | embed }}{{ zt.text }}
{% if zt.comment %}
{{ zt.comment }}
{% endif %}
{% endbq %}
