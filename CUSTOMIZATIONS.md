# Site Customizations

This file documents all custom changes made to the Digital Garden template so they can be re-applied after a template update overwrites them.

---

## Files That Are Safe to Customize (Never Overwritten by Template Updates)

- `src/site/styles/custom-style.scss` — all style overrides go here

## Files That Were Patched Manually (At Risk of Being Overwritten)

- `src/site/_includes/components/graphScript.njk` — see Graph Fix below

---

## Custom Styles (`src/site/styles/custom-style.scss`)

All of the following are in this file and will **not** be overwritten by template updates.

### 1. Wider Content Area

**Variable:** `--dg-content-max-width: 1100px` (default: `700px`)  
**Why:** The default 700px is too narrow for embedded Bases tables. Wide tables required scrolling far down the page to reach the horizontal scrollbar.

### 2. Wider Left Sidebar (Filetree)

**Variables:**
```scss
--dg-filetree-width: 300px;       /* default: 250px */
--dg-filetree-min-width: 300px;   /* default: 250px */
```
**Why:** Extra width gives more room for long note titles. Both variables must match — the content area margin is calculated from `--dg-filetree-min-width`, so mismatching them causes content to overlap the tree.

### 3. Increased Gap Between Content and Right Sidebar (Graph)

**Variable:** `--dg-sidebar-gap: 140px` (default: `80px`)  
**Why:** The local graph was overlapping the right edge of the content area at common viewport widths. Increasing the gap pushes the graph further right. Note: the sidebar auto-hides when it would still overlap, so on narrower screens the graph simply disappears rather than overlapping.

### 4. Bases Table Horizontal Scrolling

**Selector:** `.bases-embed .bases-table-container, .bases-view[data-view-type="table"]`  
**Property:** `overflow-x: auto`  
**Why:** Without this, wide embedded Bases tables cause the entire page to have a horizontal scrollbar, requiring scrolling to the very bottom of the table to reach it. This scopes the scrollbar to the table element itself.

### 5. Single-Line Note Titles in Filetree

**Selector:** `.notelink a`  
**Properties:** `white-space: nowrap; overflow: hidden; text-overflow: ellipsis`  
**Why:** Long session note titles (e.g. `1-070723-erukana-steffen-16-return-to-vardestjernen`) were wrapping onto 2–4 lines, making the filetree hard to scan. Titles now truncate with `…` and the full title is still readable on hover via the browser tooltip.

---

## Manual Patch (`src/site/_includes/components/graphScript.njk`)

**At risk:** This file is listed in `plugin-info.json` under `filesToModify`, so template updates will overwrite it.

**Problem:** The local graph showed only the home node instead of the current page's connections. Netlify normalises URLs to lowercase, but `graph.json` keys retain the original mixed casing — causing a lookup miss.

**Fix:** Replace the single-line node lookup with a three-stage lookup:

```javascript
// Before (original template code — one line)
let currentNode = remaining[currentLink] || Object.values(remaining).find((v) => v.home);

// After (patched version)
let currentNode = remaining[currentLink];
if (!currentNode) {
    const lowerCurrentLink = currentLink.toLowerCase();
    currentNode = Object.values(remaining).find((v) => v.url.toLowerCase() === lowerCurrentLink);
}
if (!currentNode) {
    currentNode = Object.values(remaining).find((v) => v.home);
}
```

**Where in the file:** Find the line containing `remaining[currentLink]` — it appears once near the top of the script block.

**After any template update:** Check whether this line was overwritten and re-apply the patch if needed.
