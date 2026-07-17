---
name: verify
description: Verify changes to the Sports Astral Forecast Terminal (single-file index.html app)
---

# Verifying this repo

Single-file app: everything lives in `index.html` (4 inline `<script>` blocks — astronomy engine, theme init, main app, sports module).

## Syntax check (fast, before browser)
```bash
node -e "const fs=require('fs');[...fs.readFileSync('index.html','utf8').matchAll(/<script>([\s\S]*?)<\/script>/g)].forEach((s,i)=>{try{new Function(s[1])}catch(e){console.log('script',i,'ERR',e.message)}});console.log('done')"
```

## Run
`preview_start {name:"sports"}` — `.claude/launch.json` serves via `python -m http.server 8123`.
Do NOT use file:// (browser pane blocks it). `computer screenshot` times out on this page — use `get_page_text` / `javascript_tool` / `read_console_messages` instead.

## Drive
- Tab sweep + error check (in javascript_tool):
  `for(t of ['match','muhurat','numero','worldclock','panchak','transit','kundali','bhav','ashtaka','kp','charts','shar','kranti','planlat','planlon']){gs({tab:t}); /* check #MAIN innerHTML for 'Error:' */}`
- Venue search: set `#iVS` value, dispatch `input` event, read `#iVSdd`.
- Team natal: `gs({natalName,natalDate:'YYYY-MM-DD',natalTime:'12',tab:'kundali'})`.
- Financial-term regression: grep each tab's innerText for `/(NIFTY|market|Bullish|Bearish|stock|trading)/i` — must be clean.

## Gotchas
- `computeAll` is memoized — any new S field that affects DATA must be added to `_memoKey`.
- The sports module is an IIFE at the end of the file; its functions are exposed via `window.tMatch` etc. and rMain uses lazy `sp('tName')` wrappers.
- Deployment: push to main → GitHub Pages (https://anki1007.github.io/sports/) rebuilds in ~1–2 min; poll with `curl | grep <new marker>`.
