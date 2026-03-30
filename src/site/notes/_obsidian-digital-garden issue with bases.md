---
{"dg-publish":true,"permalink":"/obsidian-digital-garden-issue-with-bases/","hide":true,"hideInGraph":true,"dgEnableSearch":"false","dg-note-properties":{}}
---


## Issues
Reported to https://github.com/oleeskild/obsidian-digital-garden/issues/766
- Sorting by "date" doesn't seem to work
- "Tags" are simple text, not clickable links
- Hidden notes still appear in the exported Base
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
![Pasted image 20260329184123.png](/img/user/Attachments/Pasted%20image%2020260329184123.png)
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