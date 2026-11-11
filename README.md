# UAV Swarm Trajectory Prediction and Control — OMEGA Lab project page

Project page for **Diffusion-based 4D Trajectory Prediction and Distributed Control for UAV
Swarms**, in the OMEGA Lab style.

- Paper: <https://arxiv.org/abs/2606.31197>
- Page: <https://omega-hkustgz.github.io/projects/uav-swarm-trajectories/> (live once the lab site lists it)

## Working on the page

The page is `index.html` plus `assets/`; there is no build step. Rules for agents are in
[`AGENTS.md`](AGENTS.md).

```sh
node tools/check.mjs     # what CI runs
node tools/serve.mjs     # look at it locally
```

Every pull request gets a preview link, posted on the pull request. A push to `main` asks the
lab site to republish.

## Sources

Everything on the page comes from public material. Keep this list current.

| On the page | Source |
| --- | --- |
| Title, authors, affiliations, text | arXiv 2606.31197v1 (30 Jun 2026). The text paraphrases the abstract and Sections I and III–VI; it adds no claims. The venue (IROS 2026) is the one the lab site lists for this paper as accepted; the arXiv record carries no journal reference or DOI. |
| `teaser.webp`, `framework.webp`, `dataset-trajectories.webp`, `residual-tsne.webp`, `failure-case.webp` | Figs. 1, 2, 3, 6 and 7 of the paper, rendered from the arXiv source PDFs at 2400 px wide (`pdftoppm -cropbox`, then `cwebp -q 90`). `social.jpg` is Fig. 1 on a 1200 × 630 canvas for link previews. |
| Dataset table | Table I of the paper (frame number, inter-UAV distance, speed, turning intensity), copied from the LaTeX source. The label counts are left to the paper. |
| Prediction, controller and formation tables, headline numbers | Tables II, III and IV of the paper, copied from the LaTeX source. The 16.7% and 18.2% figures and the CityNav numbers (Table V) are from Sections V-B and V-F. |
| Evidence labels | Fig. 3 shows trajectories recorded in flight for the dataset (Real-world), and is captioned as recorded data, not a run of the controller. The paper does not say on which platform the closed-loop experiments (Tables III and IV, Figs. 4 and 5) were run, and the page says so instead of labelling them. |

Not on the page because no public material exists: a code repository (so there is no Code
button), a download link for the dataset, demo video and model weights. Figs. 4 and 5 (closed-loop
curves whose platform the paper does not state) are summarised in the text, and the label counts
of Table I and the CityNav table (Table V) are left to the paper.
