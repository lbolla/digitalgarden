---
{"dg-publish":true,"permalink":"/hidden/obsidian-digital-garden-issue-with-bases/","hide":true,"dgEnableSearch":"false","dg-note-properties":{}}
---


## Issues
- Sorting by "date" doesn't seem to work
- "Tags" are simple text, not clickable links
## Example
Base query:
```
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

This renders correctly in Obsidian, but not in the exported HTML.

Obsidian:
![Pasted image 20260329184123.png](/img/user/Pasted%20image%2020260329184123.png)
HTML:
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