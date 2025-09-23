# 🔐 Adversarial Machine Learning: Paper Mapping + Hands-On Experiments

This repository combines two sides of learning and research in **Adversarial Machine Learning (AdvML)**:

1. **Systematic Paper Mapping**

   - A structured dataset of adversarial ML papers.
   - Each paper is tagged by **Threat Model × Attack Type × Modality × Evaluation Validity**.
   - Student notes summarize main questions, methods, and results.

2. **Hands-On Experiments (Jupyter Notebooks)**
   - Reproducible implementations of key adversarial attacks and defenses.
   - Experiments connect papers to practice: visualize adversarial examples, measure robustness, and test defenses.

---

## 📂 Repository Structure

```text
├── data/
│   ├── mapping.csv              # Master dataset (spreadsheet-friendly, exported from Google Sheets)
│   ├── mapping.json             # Compiled group dataset (machine-readable)
│   ├── json_group/              # Curated JSON files (approved for mapping.json)
│   │   ├── 001.json
│   │   ├── 002.json
│   │   └── ...
│   └── json_individual/         # Individual JSON outputs (per member, raw tagging)
│       ├── keigo/
│       │   ├── 001.json
│       │   └── ...
│       ├── arthur/
│       │   ├── 001.json
│       │   └── ...
│       └── shreya/
│           ├── 001.json
│           └── ...
│
├── notes/
│   ├── group/                   # Curated, polished student notes
│   │   ├── 001.md
│   │   └── ...
│   └── individual/              # Individual notes per member
│       ├── keigo/
│       │   ├── 001.md
│       │   └── ...
│       ├── arthur/
│       │   ├── 001.md
│       │   └── ...
│       └── shreya/
│           ├── 001.md
│           └── ...
│
├── notebooks/
│   ├── group/                   # Canonical, curated notebooks
│   │   ├── 01_FGSM_MNIST.ipynb
│   │   └── ...
│   └── individual/              # Personal experimentation notebooks
│       ├── keigo/
│       │   ├── FGSM_MNIST_keigo.ipynb
│       │   └── ...
│       ├── arthur/
│       │   ├── FGSM_MNIST_arthur.ipynb
│       │   └── ...
│       └── shreya/
│           ├── FGSM_MNIST_shreya.ipynb
│           └── ...
│
└── README.md

```

---

## 📝 Tagging Rules

- **No guessing.** Use `null` if info is missing.
- **Evidence required.** Cite section/figure/table for each tag.
- **Controlled vocabulary only.** Stick to glossary terms (e.g., `Image`, not `image-based`).
- **One-line plain-English summary** for each paper.

---

## 🧑‍🎓 Student Notes

Each paper has a short note in `/notes/{paper_id}.md`, which may cover:

1. Main question (1–2 sentences)
2. Key method (1 line)
3. One key result (dataset + outcome)
4. Strength & limitation
5. Applications / relevance
6. Self-check (2-min explanation + unknown terms)

---

## 🧪 Hands-On Notebooks

Interactive experiments to reinforce learning:

- .ipynb
