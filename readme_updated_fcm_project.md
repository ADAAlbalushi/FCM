# Participatory Fuzzy Cognitive Mapping: Structuring Integrated Socio-Ecological Knowledge for Heritage Management

## Overview
This project focuses on the construction, aggregation, and analysis of Fuzzy Cognitive Maps (FCMs) for heritage management research. It integrates stakeholder knowledge into computational models to support decision-making and sustainability.

The repository provides access to:
- Python scripts
- Jupyter notebooks
- Datasets
- Reproducible workflows

**The analysis consists of three main components:**
1. Individual Heterogeneity Analysis
2. FCM Construction and Aggregation
3. Collective FCM Structural and Influence Analysis

All outputs (CSV files, tables, and figures) are stored in the `Analysis and output folders` directory.

---

## Author
Amira D. — PhD Candidate, UT-ITC

---

## Repository Structure

```
FCM/
│
├── Data/                          # Original FCM matrices and labels
├── Scripts/                       # Python scripts (.py versions)
├── Tutorials/                     # Jupyter notebooks for each step
├── Analysis and output folders/   # Generated outputs
├── requirements.txt
└── README.md
```

### Tutorials Folder
The `Tutorials` folder contains Jupyter notebooks corresponding to each analysis step:

- `01_Exploring_FCMs_Properties.ipynb`
- `02_FCM_Construction_and_Aggregation.ipynb`
- `03_Collective_FCM_Structural_and_Influence_Analysis.ipynb`

These notebooks provide step-by-step explanations and visualizations of the methodology.

---

## Prerequisites

- Python 3.9+
- JupyterLab
- NumPy, Pandas, Matplotlib
- Terminal / Command Prompt access

---

## Installation and Setup

### 1. Create Project Directory

```bash
mkdir FCM
cd FCM
```

### 2. Create Virtual Environment

```bash
python -m venv venv
```

### 3. Activate Environment

**macOS / Linux**
```bash
source venv/bin/activate
```

**Windows**
```cmd
venv\Scripts\activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Launch JupyterLab

```bash
jupyter lab
```

---

## Dataset: Fuzzy Cognitive Maps

The dataset consists of CSV files representing FCM adjacency matrices.

### Data Characteristics

- Rows and columns represent concepts (C1, C2, ...)
- Cell values represent causal influence
- Positive: reinforcing
- Negative: balancing
- Zero: no relationship
- Diagonal values are always zero

Each matrix is square and labeled consistently.

---

## Workflow

The complete workflow is implemented in both Python scripts and Jupyter notebooks.

### Step 1: Exploring FCM Properties (Individual Heterogeneity)

**Script:** `exploring_fcm_properties.py`

**Notebook:** `01_Exploring_FCMs_Properties.ipynb`

Includes:
- Loading FCM matrices
- Computing degree centrality
- Calculating weighted absolute degree centrality (WADC)
- Descriptive statistics of concepts and connections

---

### Step 2: FCM Construction and Aggregation

**Script:** `fcm_construction_aggregation_with_augmentation.py`

**Notebook:** `02_FCM_Construction_and_Aggregation.ipynb`

Includes:

1. Concept Filtering
   - Applying inclusion and exclusion rules
   - Removing predefined concepts

2. Augmentation Process
   - Identifying the global concept set
   - Adding missing rows and columns
   - Filling new cells with zeros
   - Ensuring all FCMs have identical dimensions

3. Normalization and Mean Edge Calculation
   - Computing mean incoming and outgoing weights
   - Normalizing centrality measures

4. Aggregation
   - Combining relationships across FCMs
   - Calculating conditional means
   - Generating the final merged FCM

---

### Step 3: Collective FCM Structural and Influence Analysis

**Script:** `collective_fcm_structural_influence_analysis_full.py`

**Notebook:** `03_Collective_FCM_Structural_and_Influence_Analysis.ipynb`

Includes:

- Structural analysis
  - Network density
  - Centrality measures
  - Connectivity analysis

- Influence analysis
  - Scenario simulations
  - Sensitivity analysis
  - Activation dynamics

- Visualization of system behavior

---

## Running the Analysis (Python Scripts)

To run the full pipeline using scripts:

```bash
python exploring_fcm_properties.py
python fcm_construction_aggregation_with_augmentation.py
python collective_fcm_structural_influence_analysis_full.py
```

Outputs will be saved in:

```
Analysis and output folders/
```

---

## Verification Checklist

- [ ] Virtual environment activated
- [ ] All packages installed
- [ ] Data files available in `Data/`
- [ ] Scripts execute without errors
- [ ] Output files generated

---

## Troubleshooting

### Python Not Found

Try:
```bash
python3 --version
```

### Package Errors

Reinstall dependencies:
```bash
pip install --upgrade -r requirements.txt
```

### Jupyter Issues

Ensure Jupyter is installed in the active environment:
```bash
pip install jupyterlab
```

---

## Deactivating Environment

```bash
deactivate
```

---

## Contact

For questions or technical issues, please contact the author.

