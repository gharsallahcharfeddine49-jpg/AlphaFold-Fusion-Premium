AlphaFold Fusion Premium

AlphaFold Fusion Premium is an open-source, decision-oriented workflow for robust ColabFold-based protein structure prediction and confidence-aware interpretation.

The project focuses on operational robustness, reproducibility, and decision support, rather than modifying AlphaFold or ColabFold prediction algorithms.

🚀 Run in Google Colab (recommended)

The software is provided as a ready-to-run Google Colab notebook.

👉 Open directly in Colab
https://colab.research.google.com/github/gharsallahcharfeddine49-jpg/AlphaFold-Fusion-Premium/blob/main/Untitled11.ipynb

No local installation is required.

🧠 Key Features

Robust ColabFold orchestration with multi-tier MSA and JAX backend fallbacks
(GPU → GPU without plugins → CPU)

Fidelity-oriented controls: MSA strategy, recycle tuning, templates, optional relaxation

AFDB-first reuse for monomeric inputs to avoid redundant computation

Standardized confidence analytics:

pLDDT extracted from PDB / mmCIF / BCIF B-factors

pTM / ipTM parsing for multimeric assemblies (when available)

Identity mode coupling sequence identity and query coverage with structural confidence

Interactive 3D visualization with confidence-aware coloring (py3Dmol)

⚡ Quick start (Colab)

Open the Colab notebook link above

Upload or paste your FASTA sequence(s)

Select an execution profile (monomer, no-homologs, AFDB-first, etc.)

Run all cells

Inspect confidence dashboards and interactive 3D visualization

📥 Inputs

Monomers (single FASTA sequence)

Complexes (colon-delimited chains, ColabFold format)

📊 Outputs

Predicted or retrieved structures (PDB / mmCIF / BCIF)

Interactive confidence dashboards:

pLDDT distributions

empirical cumulative distribution functions (ECDF)

mean confidence scores

Comparator tables across models and AFDB hits

Interactive 3D visualization with deterministic refresh

⚙️ Execution profiles

Execution profiles map common scientific intents to predefined ColabFold parameter configurations.
They do not modify AlphaFold or ColabFold models.

Available profiles include:

Strict monomer
Disables paired MSA to analyze intrinsic folding of individual chains

No homologs
Disables structural templates for orphan or poorly characterized proteins

AFDB-first
Retrieves existing AlphaFold Database models when available

Rapid draft
Reduced-cost exploratory inference (single sequence, single model, few recycles)

Auto optimization
Adaptive parameter tuning when paired MSA or templates are disabled

🔁 Reproducibility

Each execution is isolated in a timestamped run directory containing:

input FASTA files

selected parameters

execution logs

all generated outputs

Cached MSAs and intermediate results may be reused to avoid unnecessary recomputation.

🎯 Scope and positioning

AlphaFold Fusion Premium:

does not modify AlphaFold or ColabFold inference models

introduces no new prediction algorithms

focuses on reducing execution failures, redundant computation, and
misinterpretation in routine structure prediction workflows

The term “Premium” refers to workflow completeness only.
The software is free and open-source.

✅ When should I use AlphaFold Fusion Premium?

This workflow is particularly suited for:

exploratory structure prediction in unstable or shared environments (e.g. Google Colab)

routine analysis where execution failures are common

rapid triage of candidate proteins before experimental follow-up

homology-aware interpretation of AlphaFold confidence metrics

avoiding redundant AlphaFold recomputation when AFDB structures already exist

❌ When should I NOT use this?

AlphaFold Fusion Premium is not intended for:

benchmarking or improving AlphaFold prediction accuracy

replacing AlphaFold, ColabFold, or AlphaFold3 inference

high-throughput proteome-wide prediction pipelines

functional annotation or experimental validation

📦 Implementation

Language: Python

Interface: Streamlit

Main dependencies include:

ColabFold

JAX / JAXlib

MMseqs2

Gemmi

Biopython

Plotly

py3Dmol / 3Dmol.js

📚 Citation

If you use AlphaFold Fusion Premium in academic work, please cite:

Charfeddine G.
AlphaFold Fusion Premium: a decision-oriented workflow for robust ColabFold-based protein structure prediction and confidence-aware interpretation.
Bioinformatics (submitted).

(Replace with DOI once available.)

📄 License

MIT License.

⚠️ Disclaimer

This project is not affiliated with Google DeepMind or EMBL-EBI.
