# free-llm-radar-data

Offer data for the **Free LLM Radar** dashboard, served over GitHub Pages so the dashboard
can read it cross-origin.

- `data.js` — sets `window.RADAR`. Rewritten by a scheduled refresh job.
- Served at: https://ericagulto.github.io/free-llm-radar-data/data.js

This repo holds **data only**. The dashboard itself lives in `free-llm-radar`.

The split exists so a daily data refresh does not require redeploying the site. GitHub Pages
serves `.js` as `application/javascript` with `access-control-allow-origin: *`, which is what
makes the cross-origin load work.

The `id` values in `data.js` are permanent keys referenced by the dashboard's referral layer.
Do not rename them.
