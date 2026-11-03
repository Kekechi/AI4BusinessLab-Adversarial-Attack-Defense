# Adversarial ML — Reading Group Experiments and Mapping Scheme

Reading notes and hands-on experiments from an undergraduate adversarial-ML reading group in
the SDSU AI4Business Lab, 2025. Two attacks are implemented and measured with ART. A
paper-mapping scheme was designed but not completed — see *What didn't happen* below.

## What's here

### Experiments — `notebooks/individual/keigo/`

- `experiment_note_fashin_mnist_fgsm.ipynb` — FGSM on Fashion-MNIST via ART (2025-09-18)
- `experiment_note_fashin_mnist_pgd.ipynb` — PGD on Fashion-MNIST via ART (2025-10-15)
- `experiment_note_template.ipynb` — the template both follow
- `adversarial_fgsm.ipynb`, `classification.ipynb` — worked through from the TensorFlow tutorials

Both experiment notes use the same structure: objective, hypothesis and success criteria stated
*before* the run; environment captured from the machine (`pip show`, `/etc/os-release`) rather
than asserted; then dataset, model, attack config, results, visualization.

Same architecture (Flatten → Dense 128 → Dense 10), same training recipe and same ε grid in
both, so the two attacks are comparable:

| ε     | FGSM accuracy | PGD accuracy |
| ----- | ------------- | ------------ |
| clean | 0.8805        | 0.8850       |
| 0.01  | 0.8070        | 0.8088       |
| 0.05  | 0.2955        | 0.1935       |
| 0.10  | 0.1532        | 0.0791       |
| 0.20  | 0.0875        | 0.0732       |

PGD is the stronger attack at every ε ≥ 0.05, as expected. These reproduce known results on a
small model — the point was the method, not the finding. The two runs trained separate model
instances, so clean accuracy differs slightly: conditions are matched, weights are not.

### Reading notes — `notes/individual/keigo/`

Eight notes (`003`–`010`) in a fixed format: main question, key method, main results, strengths
and limitations, relevance, and a self-check that lists terms not yet understood. The format is
in `template/000.md`.

### Environment — `docker/`

Multi-stage image with CPU and GPU targets, Compose profiles and pinned dependencies, so
everyone runs the same stack.

```bash
docker compose up notebook-cpu          # CPU
docker compose --profile gpu up notebook-gpu
```

### Mapping scheme — `data/`

A five-axis tagging scheme — threat model × modality × attack type × representative method ×
evaluation validity — with a controlled glossary, an assignee plus second-reviewer workflow, and
three rules: no tags without evidence, leave blank if unsure, always write a one-line
plain-English summary. `data/json_individual/keigo/` holds seven tagged entries.

## What didn't happen

The mapping was meant to cover a corpus of roughly 1000 papers and produce a curated group
dataset. **It didn't.** `data/json_group/` and `notebooks/group/` are empty, and there is no
`mapping.csv` or `mapping.json`.

The binding constraint turned out to be domain foundation rather than process: tagging a paper
usefully requires understanding it first, and the group was still building that understanding.
The response was to slow down — reading groups, a small set of foundational papers (Goodfellow
et al. 2015 on FGSM, Madry et al. 2017 on PGD and adversarial training) read properly, and
deadlines moved to protect comprehension over throughput.

The scheme and the workflow are kept here because they are reusable. The dataset they were
designed to produce does not exist, and nothing in this repository should be cited as one.

## References

- Goodfellow, Shlens & Szegedy, *Explaining and Harnessing Adversarial Examples* (2015) —
  <https://arxiv.org/abs/1412.6572>
- Madry et al., *Towards Deep Learning Models Resistant to Adversarial Attacks* (2017) —
  <https://arxiv.org/abs/1706.06083>
- Adversarial Robustness Toolbox — <https://github.com/Trusted-AI/adversarial-robustness-toolbox>
