---
{"dg-publish":true,"permalink":"/02 Player/Erukana (Nissen)/bases/Taxonomy - People/","tags":["erukana","reference","taxonomy","metadata"]}
---


# Taxonomy Reference - People

This document defines the standardized metadata fields for People files in the Erukana vault. Use these fields in YAML frontmatter to enable consistent searching and querying.

---

## Frontmatter Template

```yaml
---
dg-publish: true
category: npc
race:
role:
  -
social_status:
affiliation:
  -
disposition:
status:
location_primary:
Campaign: Erukana
tags: [erukana, npc]
---
```

---

## Field Definitions

### `category`
What type of entry this is.

| Value | Description |
|-------|-------------|
| `npc` | Non-player character |
| `pc` | Player character |
| `deity` | God or divine entity |
| `title` | Rank or position reference (not a specific person) |
| `creature` | Monster or creature type |

---

### `race`
The character's species or ancestry.

| Value | Description |
|-------|-------------|
| `human` | Human |
| `dwarf` | Dwarf (Bjergenes Børn) |
| `elf` | Elf (including Ellin Thalor, vilde elvere) |
| `gnome` | Gnome |
| `half-giant` | Half-giant (Nordheim heritage) |
| `orc` | Orc |
| `kobold` | Kobold |
| `goblin` | Goblin |
| `hybrid` | Mixed race or transformed (e.g., half-deer, avatar) |
| `undead` | Undead creature |
| `unspecified` | Race not mentioned in sources |

---

### `role`
The character's function in the story. Can have multiple values.

| Value | Description | Examples |
|-------|-------------|----------|
| `nobility` | Rulers, lords, ladies, barons | Baron Zhaarko, Hertug Robert De Ros |
| `military` | Soldiers, guards, officers | Vagtkaptajn Samuel, Hans Baudler |
| `religious` | Priests, clerics, temple workers | Beril Højmølle, Tyra Volkmarr, Edmund Vitano |
| `merchant` | Traders, shopkeepers, guild members | Assana Lemieux, Illyria Starmantle |
| `resistance` | Rebels, freedom fighters | Fafnir, Samy |
| `antagonist` | Villains, enemies, hostile NPCs | Arakas Zhaarko, Ulrik Stadtfelt |
| `commoner` | Workers, farmers, townsfolk | Krugge, Elvira, Håkan |
| `scholar` | Historians, sages, researchers | Jarell Flick, Archibald Oddsmoke |
| `spy` | Informants, agents, intelligence | Maria, Vallis |
| `druid` | Nature priests, forest guardians | Seiran, Corwin |
| `pirate` | Sea raiders, smugglers | Pirat kaptajnen Arlis, Zarafine |
| `paladin` | Holy warriors, knights | Sir Winston, Evelyn Adair |
| `shaman` | Tribal spiritual leaders | Urza |
| `servant` | Household staff, attendants | Pierre, Orlock Helmsveil |

---

### `social_status`
The character's place in society.

| Value | Description |
|-------|-------------|
| `royalty` | Kings, queens, avatars of gods |
| `duke` | Dukes, duchesses (Hertug/Hertuginde) |
| `baron` | Barons, baronesses |
| `lord` | Lords, ladies (lower nobility) |
| `knight` | Knighted individuals (Sir/Dame) |
| `officer` | Military officers (Marskal, Kaptajn) |
| `priest` | Religious leaders |
| `merchant` | Trading class |
| `commoner` | Common folk, workers |
| `criminal` | Outlaws, thieves |
| `outcast` | Exiles, tribal outsiders |
| `servant` | Household servants |

---

### `affiliation`
Organizations, factions, or groups the character belongs to. Can have multiple values.

#### Major Factions
| Value | Description |
|-------|-------------|
| `The Queensguard` | Holy order serving Queen Neferata |
| `Ridderne af Blodrosen` | The Rose Knights (antagonist faction) |
| `Astley Avengers` | The player character group |
| `Azur Ordenen` | The Azure Order (mages) |

#### Resistance & Underground
| Value | Description |
|-------|-------------|
| `Fafnirs modstandsgruppe` | Fafnir's resistance movement |
| `Jernkniven` | Thieves' guild |

#### Noble Houses
| Value | Description |
|-------|-------------|
| `House Leitner` | Leitner family (antagonists) |
| `House De'Evers` | De'Evers family (Mistville) |
| `Adelhuset Vitano` | House Vitano |
| `Familien Botreaux` | Botreaux family |

#### Merchant Organizations
| Value | Description |
|-------|-------------|
| `Waning Moon` | Waning Moon merchant house |
| `Merchant Konglomeratet` | Merchant consortium |

#### Dwarf Factions
| Value | Description |
|-------|-------------|
| `Slatestone` | Traditional dwarf halls |
| `Silverstream` | Progressive dwarf halls |
| `Stenvogterne` | Stone Wardens |

#### Tribal/Monster Factions
| Value | Description |
|-------|-------------|
| `Rød tand stammen` | Red Tooth orc tribe |
| `Dark Gem klanen` | Corrupted kobold clan |
| `Knoglestammen` | Bone Tribe (orcs) |
| `Zazmir stamme` | Zazmir tribe |
| `Slette folket` | Plains people |
| `Horden` | The Horde (greenskins) |

#### Religious
| Value | Description |
|-------|-------------|
| `Bahamuts Tilhængere` | Secret Bahamut worshippers |
| `Opal kulten` | Opal cult (demon worshippers) |

---

### `disposition`
The character's relationship to the player party.

| Value | Description |
|-------|-------------|
| `ally` | Friendly, helpful to the party |
| `neutral` | Neither friendly nor hostile |
| `enemy` | Actively hostile to the party |
| `unknown` | Relationship not established |
| `conditional` | Depends on circumstances |
| `deceased-ally` | Was an ally, now dead |
| `deceased-enemy` | Was an enemy, now dead |

---

### `status`
The character's current state.

| Value | Description |
|-------|-------------|
| `alive` | Living |
| `dead` | Deceased |
| `undead` | Undead (vampire, zombie, etc.) |
| `missing` | Whereabouts unknown |
| `unknown` | Status not established |
| `transformed` | Changed state (cocoon, petrified, etc.) |

---

### `location_primary`
Where the character is primarily found or associated with.

#### Cities & Towns
- `Astley` - Main city
- `Mistville` - Town near Astley
- `Blackforge` - Mowbray capital

#### Baronies & Regions
- `Baroniet Eresby`
- `Baroniet Welles`
- `Baroniet Mowbray`
- `Baroniet Blackmere`
- `Baroniet Valence`
- `Hertugdømmet Botreaux`
- `Nordheim` / `Nordlandet`

#### Special Locations
- `Anaksa` - Queensguard homeland
- `Feywood` - Forest region
- `Grøndalen` - Valley region
- `Silverstream dværgehallerne`
- `Slatestone dværgehallerne`

---

## Example: Complete Entry

```yaml
---
dg-publish: true
category: npc
race: dwarf
role:
  - resistance
  - military
social_status: commoner
affiliation:
  - Fafnirs modstandsgruppe
disposition: ally
status: alive
location_primary: Astley
Campaign: Erukana
tags: [erukana, npc, dwarf, resistance, anti-blodrosen]
---

## Description
Fafnir er en dværg og tidligere lejesoldat...
```

---

## Dataview Query Examples

### Find all allies
| File | race | role | location_primary |
| ---- | ---- | ---- | ---------------- |

{ .block-language-dataview}

### Find resistance members
| File | race | disposition | status |
| ---- | ---- | ----------- | ------ |

{ .block-language-dataview}

### Find characters by race
| File | role | affiliation | disposition |
| ---- | ---- | ----------- | ----------- |

{ .block-language-dataview}

### Find enemies in a location
| File | race | role | affiliation |
| ---- | ---- | ---- | ----------- |

{ .block-language-dataview}

### Find all nobility
| File | race | affiliation | location_primary |
| ---- | ---- | ----------- | ---------------- |

{ .block-language-dataview}

---

## Search Syntax

In Obsidian's search, you can find characters by metadata:

- `race:dwarf` - All dwarves
- `role:resistance` - All resistance fighters
- `disposition:ally` - All allies
- `affiliation:"The Queensguard"` - All Queensguard members
- `status:dead` - All deceased characters
- `race:dwarf role:resistance` - Dwarf resistance fighters

---

## Notes

- **Multiple values**: `role` and `affiliation` can have multiple values as lists
- **Consistency**: Always use lowercase for field values
- **Unknown**: Use `unspecified` or `unknown` rather than leaving blank
- **Updates**: Update `status` and `disposition` as the campaign progresses
