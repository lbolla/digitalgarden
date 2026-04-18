---
{"dg-publish":true,"permalink":"/reading/the-shelf/","pinned":"true","created":"2026-03-29","dg-note-properties":{"date":"2026-03-29"}}
---


```base
filters:
  and:
    - file.folder == "Reading/Books"
views:
  - type: cards
    name: Cards
    order:
      - file.name
      - author
      - file.tags
      - date
    sort:
      - property: date
        direction: DESC
    image: image
    imageFit: contain
    imageAspectRatio: 1.4

```
