# Manufacturing Planner — data flow

A one-page visual explanation of a production planning system: what data goes
in, where the decision gets made, and where each result appears on screen.

**Live page:** https://srkale12.github.io/Planner_for_Manufacturing/

## What the system does

A factory makes hundreds of products on a handful of production lines. Every
week somebody decides what to make, on which line, on which day, and how much —
balancing order fulfilment against inventory investment against changeover time.
This is the system that makes that decision.

- Builds a twelve-week plan across multiple production lines in about 90 seconds
- Weighs four competing goals at once: filling customer orders, holding safety
  stock, avoiding excess inventory, and using shifts efficiently
- Sequences production day by day so compatible products run together and lines
  spend less time being washed out between runs
- Python / FastAPI backend, React frontend, SQL data layer
- Ships three ways from one codebase: hosted web app, Windows desktop installer,
  and an ERP connector

It recommends; it never writes to a system of record. A planner reviews every
proposal, the ERP creates the actual production orders, and every recommendation
is logged with who ran it and what it said.

## This repository

Contains the explainer page only — a single self-contained HTML file with no
build step, no dependencies, and no external requests. The planner source is
not public.

```
index.html     the page
preview.png    link-preview image (optional; see below)
```

## Link previews

`index.html` carries Open Graph tags so the page renders as a card when shared.
Two values must be absolute URLs pointing at the live site — update them if the
repository name or account changes:

- `og:url`
- `og:image` → expects `preview.png` (1200×630) in this folder

Figures shown in the example walkthrough are illustrative, not production data.
