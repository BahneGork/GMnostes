---
{"dg-publish":true,"permalink":"/02 Player/Erukana (Nissen)/bases/People Database/","dg-note-properties":{"type":"npc","subtype":"base"}}
---




```base
filters:
  and:
    - file.folder.contains("Erukana")
    - file.tags.contains("npc")
    - '!file.name.contains("_Erukana")'
views:
  - type: table
    name: People
    order:
      - file.name
      - faction
      - affiliation
      - aliases
      - category
      - disposition
      - location
      - Profession
      - race
      - role
      - sessions
      - social_status
      - status

```
