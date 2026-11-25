# Food Kundali

Apna khana, apni kundali — food nutrition app (single-page, offline).

## Files (5)

| File | Kya hai |
|---|---|
| `index.html` | Page ka structure (header, search box, dialogs) + file links |
| `style.css` | Saara design — colors, layout, dark theme, mobile, animations |
| `data.js` | Saara data — 264 foods ke nutrition values, nutrients, English/Hinglish text |
| `core.js` | Chhote helper functions + database (load/save) + benefits ranking |
| `features.js` | Saare features — Food detail, Search, Calculator, Nutrients, Compare, Diary, Profile, Share image, "Why should I eat" |

## Kaise chalega

```bash
cd food-kundali
python3 -m http.server 8000
# Browser mein kholein: http://localhost:8000
```

Ya file ko double-click karke bhi khul sakta hai (koi build step nahi hai).

## Edit karna ho to

- **Design/color badalna hai** → `style.css`
- **Food data add/edit karna hai** → `data.js` (SEED / FOOD_ADD sections)
- **Naya feature ya logic** → `features.js`
- **Text (English/Hinglish)** → `data.js` (LANG section)

## Dhyaan rahe

- Files ka **load order fix hai**: `data.js` → `core.js` → `features.js`. Order mat badlo.
- Function names, HTML IDs, aur `fk_*` localStorage keys **mat badlo** — user ka saved data (diary, profile) inhi par depend karta hai.
- Original single-file backup: `../Food Kundali.original.html`
