# LatentCapacityCut — prototypes

Live site (Vercel): https://capacity-navy.vercel.app/ — serves `index.html`.

| File | What it is |
|---|---|
| `index.html` | **What is live.** Currently a copy of `growth-dashboard-latent.html`. |
| `growth-dashboard-latent.html` | Growth Dashboard (Latent) — top cards + metrics (Needs attention / Good) + Growth Graph, week filter, version switcher. |
| `capacity-cuts-dc-capacity.html` | Capacity Cuts dashboard (DC Capacity → Capacity Cuts tab). Kept up to date, not live. |

## Switch what is live

```bash
# make Capacity Cuts live again
cp capacity-cuts-dc-capacity.html index.html && git commit -am "Live: Capacity Cuts" && git push

# make Growth Dashboard live again
cp growth-dashboard-latent.html index.html && git commit -am "Live: Growth Dashboard" && git push
```

The tag `capacity-cuts-v1` marks the last commit where Capacity Cuts was live (`git checkout capacity-cuts-v1 -- index.html`).

Each HTML file is standalone (fonts, icons, CSS and JS inlined). Source lives in `growth-dashboard/screens/` and is built with `tools/build-share.py <source.html> <out.html>`.
