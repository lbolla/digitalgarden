---
{"dg-publish":true,"permalink":"/todo/","hide":true,"dg-note-properties":{}}
---

- [ ] Have a bunch of "related pages" on the end or sidebar: use dataview select by similar tags, sort by date
	Use "components" of digital-garden
	[theme switcher](https://github.com/uroybd/topobon/blob/a4361f90e29bddf38c9e088c82354913f88514a3/src/site/_includes/components/user/common/footer/001-floatingControls.njk#L47) used [here](https://hermitage.utsob.me/)
- [ ] Gist font too big on mobile
- [ ] "Reading log" pages (and template)
	Inspiration: The Shelf https://hermitage.utsob.me/reading/the-shelf/
- [ ] digital garden supports "random" note?
- [ ] favicon
- [ ] Do we need dataview??
	- Hide base header
## Problems with bases and digital-garden
- Sorting by "date"
- "Tags" not clickable
- Odd "image" rendering and size
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
      - file.tags
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
## Drafts
```base
filters:
  and:
    - file.hasTag("draft")
views:
  - type: list
    name: Table
    filters:
      and:
        - file.folder != "Templates"
    order:
      - file.name
      - date

```
