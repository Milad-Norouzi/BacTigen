# Training Datasets for BacTigen Machine Learning Model

This folder contains the curated protein sequence datasets used to train the BacTigen machine learning model for protective antigen prediction.

---

## 📊 Dataset Summary

| Dataset | Source | Number of Sequences | Label in Header |
|:---|:---|:---:|:---|
| **Positive** | Protegen database | **660** | `\|Positive` |
| **Negative** | UniProt bacterial proteomes | **1,000** | `\|Negative` |

---

## 📄 File Format

All sequences are in standard **FASTA format**. Each header includes a label (`Positive` or `Negative`) after the `|` character, indicating the class membership.

**Example headers:**
Protegen,3|VO,VO_0010856|PMID,10816475,|Positive
ZAPB_SERP5;Serratia_proteamaculans;9240_Da|Negative




---

## 🔬 Dataset Construction

### Positive Dataset (660 sequences)
- Obtained from the **Protegen** database, which contains manually curated experimentally validated protective antigens.

### Negative Dataset (1,000 sequences)
- Retrieved from **UniProt** bacterial proteomes.
- Built using a multi‑stage filtering strategy:
  1. **Motif‑based filtering** – removal of sequences containing conserved motifs found in positive antigens.
  2. **Redundancy reduction** – CD‑HIT clustering at 80% sequence identity.
  3. **Homology filtering** – removal of sequences with >30% identity to positive antigens (BLASTp).
  4. **Diversity selection** – k‑means clustering on Word2Vec embeddings, selecting one representative from each of 1,000 clusters.

---


## 📁 Files

- `training_datasets.fasta` – 660 protective antigens and 1,000 non‑protective proteins
---

## ⚠️ Notes

- These datasets are provided for **research purposes only**.
- The negative dataset is a carefully curated proxy, not a gold‑standard set of non‑protective antigens.

---

**© 2026 – BacTigen – Automated Reverse Vaccinology Platform**
