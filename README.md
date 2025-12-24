# AlphaFold Fusion Premium

**AlphaFold Fusion Premium** is an open-source, decision-oriented workflow for
robust ColabFold-based protein structure prediction and confidence-aware
interpretation.

The project focuses on **operational robustness, reproducibility, and
decision support**, rather than modifying AlphaFold or ColabFold prediction
algorithms.

---

## 🚀 Run in Google Colab (recommended)

The software is provided as a ready-to-run Google Colab notebook.

👉 **Open directly in Colab**:  
https://colab.research.google.com/github/gharsallahcharfeddine49-jpg/AlphaFold-Fusion-Premium/blob/main/AlphaFold_Fusion_Premium.ipynb

No local installation is required.

---

## 🧠 Key Features

- Robust ColabFold orchestration with multi-tier MSA and JAX backend fallbacks  
  *(GPU → GPU without plugins → CPU)*
- Fidelity-oriented controls: MSA strategy, recycle tuning, templates, optional relaxation
- **AFDB-first reuse** for monomeric inputs to avoid redundant computation
- Standardized confidence analytics:
  - pLDDT extracted from PDB/mmCIF/BCIF B-factors
  - pTM / ipTM parsing for multimeric assemblies (when available)
- **Identity mode** coupling sequence identity and query coverage with structural confidence
- Interactive 3D visualization with confidence-aware coloring (py3Dmol)

---

## 📥 Inputs

- **Monomers**
- **Complexes**

---

## 📊 Outputs

- Predicted or retrieved structures (PDB / mmCIF / BCIF)
- Interactive confidence dashboards (pLDDT distributions, ECDF, mean score)
- Comparator tables across models and AFDB hits
- Interactive 3D visualization with deterministic refresh

---

## 🎯 Scope and Positioning

AlphaFold Fusion Premium:
- **does not modify** AlphaFold or ColabFold inference models
- **introduces no new prediction algorithms**
- focuses on reducing execution failures, redundant computation, and
misinterpretation in routine structure prediction workflows

The term *“Premium”* refers to workflow completeness only.
The software is **free and open-source**.

---

## 📦 Implementation

- Language: Python
- Interface: Streamlit
- Main dependencies:
- ColabFold
- JAX / JAXlib
- Gemmi, Biopython
- Plotly
- py3Dmol / 3Dmol.js

---

## 📄 License

MIT License.

---

## ⚠️ Disclaimer

This project is **not affiliated with Google DeepMind or EMBL-EBI**.

