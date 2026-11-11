# AFFORD-X

Project page for **AFFORD-X: Affordance-Grounded Agentic Policy for Zero-Shot Robot Manipulation**.

AFFORD-X separates what a robot *can* do from what it *should* do inside a zero-shot agentic loop with frozen
SAM 3 and Gemini: perceive, gate contacts on feasibility, order them by contact mechanics and task affordance, act,
verify, and replan.

Live at <https://physical-super-intelligence.github.io/AFFORD-X/>.

## Where the numbers come from

Every number and figure on the main page is taken from the paper (CVPR 2027 author kit, `main.tex` and `sec/*.tex`):

| Page section | Paper source |
|---|---|
| Teaser | `figures/fig_teaser_v3.pdf` (`fig:teaser`) |
| Method | `figures/fig_framework.pdf` (`fig:framework`), `figures/fig_map_vs_affordx.pdf` (`fig:map`) |
| LIBERO-PRO | Table `tab:libero` (the six cells every method reports), `figures/fig_rollouts.pdf` |
| Meta-World MT50 | Table `tab:mt50` |
| Real robot | Table `tab:real`, `figures/fig_real_robot.pdf` |
| Where the VLM sits | Table `tab:vlm`, `figures/fig_qualitative.pdf` |

The figures are rendered from the paper PDFs at 2400 px wide. The loop videos are logged recoveries replayed from the
agentic-loop runs, and the three 3D explorers (`gate-3d.html`, `rollouts-4d.html`, `handle-points.html`) are
supplementary views built from logged runs, each with its own data under `static/js/`.

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Structure

```
index.html                 # the page
gate-3d.html, rollouts-4d.html, handle-points.html   # 3D explorers
static/css/index.css       # styles
static/js/index.js         # nav, tables, lightbox, BibTeX copy
static/js/gate_scenes/, handle_points/, rollouts_4d/ # explorer data
static/images/             # paper figures
static/videos/loop/        # agentic-loop recovery videos and posters
```
