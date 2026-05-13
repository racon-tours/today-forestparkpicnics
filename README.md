# today-forestparkpicnics

Static checklist pages for picnic-helper setup days. Deployed at **today.forestparkpicnics.com**.

- `/ah/` → Art Hill (lunch) checklist
- `/pl/` → Pagoda Lake (dinner) checklist
- `/` → simple picker between the two

Reads items from the **Today Checklists** Google Sheet (Drive ID `1235TZ4Nh2bRzew7QJ1Vpx8R3EfTyVP33zd0H4Sb2ByU`), tabs `ah` and `pl`, via gviz CSV. Sheet must be shared "Anyone with the link → Viewer".

## State

LocalStorage, keyed by `tab:YYYY-MM-DD:rowIndex`. Stale keys from previous days are pruned on each page load → fresh checklist every morning.

## Edit the checklist

Open the **Today Checklists** sheet, ah or pl tab. Columns: `section | item | notes`. Page picks up changes within ~5 min (Google CSV cache); hit ↻ in the header to force a refresh.
