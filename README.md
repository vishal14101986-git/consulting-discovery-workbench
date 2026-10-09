# Consulting Discovery Workbenches

Single-page workbenches for running customer discovery workshops in the browser. Each one walks a consultant through engagement setup, business outcomes, a maturity assessment, a use-case map and a generated readout.

**Live demo:** __PAGES_URL__

| Workbench | Path | Areas |
|---|---|---|
| AI & Apps Discovery | [`ai/`](ai/index.html) | AI & agents · App modernisation · Low-code & Copilot · Data & integration (25 questions) |
| OpenShift Discovery | [`openshift/`](openshift/index.html) | Platform · Apps & DevEx · Security & compliance · Operations & automation · Virtualization · AI workloads (28 questions) |

## Features

- **Guided stages:** engagement, business outcomes, one stage per assessment area, use-case map and readout.
- **1–5 maturity scoring:** every question has anchor descriptions plus a recommendation and the products that address it.
- **Signals and notes** captured per area.
- **Value × feasibility matrix** with a library of common use cases.
- **Generated readout:** readiness by area, recommended engagements, gaps with solutions, and a 30/60/90-day plan.
- **Export:** copy the readout as Markdown, or copy/load the full session as JSON.
- **Private by design:** no backend. Sessions autosave to the browser's `localStorage` only.
- Light and dark themes; works on phones and tablets.

## Run locally

The pages are plain HTML with inline CSS and JavaScript, with no build step and no dependencies. Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 5173
# then open http://localhost:5173
```

## Customise

Each workbench keeps its content in one block near the top of its `<script>`:

- `PILLARS`: assessment areas, signals, questions, anchors, recommendations and products
- `TEMPLATES`: use-case library
- `INDUSTRIES`, `STAKE`, `FOOT`, `PRIOS`: setup and outcome options
- `compute()`: rules that turn scores and signals into recommended engagements
- `sample()`: the fictional sample customer shown on first load

To add another practice (for example AWS or SAP), copy one folder, replace that content, change the `KEY` constant so sessions don't collide, and add a card to the root `index.html`.

## Notes

Sample customers (Kōwhai Health, Tūī Bank) are fictional. Product names belong to their respective owners; this project is not affiliated with or endorsed by Microsoft or Red Hat.

## License

[MIT](LICENSE)
