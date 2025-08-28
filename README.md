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
│ ├── mapping.csv # Master dataset (spreadsheet-friendly)
│ ├── mapping.json # Machine-readable dataset
| └── json/              # Individual JSON files (one per paper)
|  ├── 001.json
|  ├── 002.json
|  ├── 003.json
|  └── ...
│
├── notes/
│ ├── 001.md # Student note 
│ ├── 002.md
│ └── ...
│
├── notebooks/
│ ├── 01_FGSM_MNIST.ipynb
│ ├── 02_PGD_CIFAR10.ipynb
│ ├── 03_Adversarial_Training.ipynb
│ └── ...
│
├── src/
│ ├── attacks.py # FGSM, PGD implementations
│ ├── models.py # Simple CNNs for MNIST/CIFAR
│ └── eval.py # Evaluation utilities
│
├── scripts/
│ ├── csv_to_json.py # Convert CSV → JSON
│ └── validate_tags.py # Ensure glossary compliance
│
├── outputs/
│ ├── figures/ # Visualizations
│ ├── logs/ # CSV logs of experiments
│ └── checkpoints/ # Saved models
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
Each paper has a short note in `/notes/{paper_id}.md` covering:
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
