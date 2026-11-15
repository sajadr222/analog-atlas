# AnalogAtlas — Team Nebulabs (NASA Space Apps Challenge 2026)

A website that shows where on Earth looks like Mars, using our model's results.

## Open it
- Easiest: open `AnalogAtlas.html` (one file, works offline).
- Or serve this folder (`python3 -m http.server`) and open `index.html`. It then reads the files in `data/` directly.

## Data (used exactly as the model produced it)
| File | What it is |
|---|---|
| `data/results.json` | Model output: `meta` + `sites[]` (one 3° square each: `site_id`, `lat`, `lon`, `mars_score`, `top_features[]`, `is_known`) |
| `data/candidates.json` | Top new places with their 7 measured values |
| `data/known_sites.json` | The NASA analog sites the model learned from |
| `data/feature_names.json` | The 7 signs the model uses |
| `data/feature_importance.json` | Global importance of each sign (from the training notebook) |
| `data/data.js` | The same five files in one script, so the page works when opened from disk |

To update: replace the JSON files with new model output and rebuild `data/data.js`, or use **For the team → Load model results** on the page to try a new `results.json` without changing any file.

Site names, NASA links and summaries for the known sites come from official NASA pages. Candidate area names are approximate labels for the coordinates.
