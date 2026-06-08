# Deep Coverage — Product Counsel

An offline, self-contained coverage diagnostic for in-house product counsel.

The premise, adapted from the investment-bank coverage model: the durable value of counsel
isn't faster work product (AI commoditizes the answers, and teams start to self-serve and route
around you). The durable value is *coverage* — being the counsel who saw it in the spec, who
carries context no tool has, who is in the room before the decision hardens. This tool maps the
eight dimensions of that coverage and shows the gap between where attention goes today and where
full coverage would put it.

## Files

- **`index.html`** — the tool. Opens on **My read** (individual self-assessment) and includes a
  **Team roll-up** tab.
- **`radar-solo.html`** — the single-mode individual radar only, for a stripped-down version.

Both files are fully self-contained: no dependencies, no build step, no network calls, no storage.
They run from any browser, locally or hosted. Nothing is transmitted.

## How it works

**My read** — set eight sliders 0–10, edit any label to fit your org, then click *Copy my read*
to get a short portable code (`DCR1:...`). Send that code to whoever is rolling up.

**Team roll-up** — paste everyone's codes, one per line, and click *Build the picture*. It draws
each person as a faint line, the team average as the solid shape, and ranks the eight axes by where
the team is least covered.

Reads aggregate by axis **position** (1–8), not by label text. For clean roll-ups, lock the eight
labels before distributing and ask the team to leave them as-is.

## Publish with GitHub Pages

1. Repo **Settings → Pages**.
2. Source: **Deploy from a branch** → `main` → `/ (root)`.
3. Live at **https://kenpriore.github.io/productcounsel/**

A single HTML file needs no Jekyll config or anything else. To use a custom domain (e.g.
kenpriore.ai), add a `CNAME` file and the matching DNS record.
