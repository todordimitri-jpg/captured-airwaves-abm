# Captured Airwaves (NetLogo model)

NetLogo 7.0.4 model that accompanies my individual research proposal for *Foundations of Computational Social Science* (MSc in Computational Social Science, UC3M, 2026).

**Question:** how many points of support can a ruling party gain from controlling most of the television, radio and press, when people also talk to their neighbours and read social media? The setting is Serbia during the 2024–2025 student protests.

## Files

| File | What it is |
|---|---|
| `captured-airwaves.nlogox` | The model: code, interface and all BehaviorSpace experiments |
| `results/check-benchmark.csv` | Test run: 10 repetitions at media-control 0.5 and 0.9 |

## Running it

1. Open `captured-airwaves.nlogox` in NetLogo 7.0.4 or later.
2. Press **setup**, then **go**. One tick is one day.
3. Red agents support the ruling party, blue ones do not. The darker agents are committed (loyalists or activists) and never change.
4. *Tools → BehaviorSpace* lists the experiments: `E1-media-x-age`, `E2-committed`, `E3-space`, `E4-*` (robustness), `long-run-check` and `check-benchmark`.

## Main parameters

| Slider | Default | Meaning |
|---|---|---|
| `media-control` | 0.90 | Share of traditional-media messages favourable to the government |
| `social-critical` | 0.70 | Share of social-media messages critical of the government |
| `older-share` | 0.40 | Share of agents in the older group |
| `tv-reliance-older` / `-younger` | 0.80 / 0.25 | How much of each group's media use is traditional media |
| `peer-weight` | 0.50 | Chance that an update comes from a neighbour rather than from media |
| `loyalist-share` / `activist-share` | 0.10 / 0.05 | Committed supporters / committed opponents |
| `update-prob` | 0.20 | Daily chance that an agent reconsiders its position |
| `density` | 0.80 | Share of occupied patches |
| `clustered-activists?` | off | Activists spread out, or grouped in one district |

The `benchmark` monitor shows the mean-field prediction. In the test run, the model gives 46.3% support with balanced media (benchmark 46.5%) and 60.1% with 90% media control (benchmark 60.4%).

## Credits

Todor Dimitrijevic, 2026. The neighbour-copying rule is the voter model as taught in the course (A. Sánchez, lecture notes, ch. 6). The code was written with the help of Claude (Anthropic).
