---
{"dg-publish":true,"permalink":"/lorenzo-bolla/","hide":true,"tags":["gardenEntry"],"dgShowBacklinks":"false","dg-note-properties":{}}
---


Hi! I'm Lorenzo Bolla, [[Curriculum Vitae\|Software Developer]] in Zűrich, CH.

When I'm not programming in [Python](https://www.python.org/), [Rust](https://www.rust-lang.org/en-US/), [Erlang](https://www.erlang.org/), [Go](https://golang.org/), [Haskell](https://www.haskell.org/) or [Java](http://openjdk.java.net/) I am playing either basketball, piano or chess.

## Latest notes
```base
filters:
  and:
    - file.folder != "Templates"
views:
  - type: table
    name: Table
    order:
      - file.name
      - date
      - tags
    sort:
      - property: date
        direction: DESC
    limit: 5

```

## Reading
```base
filters:
  and:
    - file.folder == "Books"
    - file.tags.contains("reading")
views:
  - type: cards
    name: Cards
    order:
      - file.name
    sort:
      - property: date
        direction: ASC
    image: image
    imageFit: contain

```
See also [[The Shelf\|The Shelf]].