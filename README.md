# Participatory Fuzzy Cognitive Mapping: Structuring Integrated Socio-Ecological Knowledge for Heritage Management
## overview
- This project focuses on the construction and analysis of Fuzzy Cognitive Maps (FCMs) as part of a research project related to heritage management. FCMs are used for modeling the relationships and impacts of various concepts within the system, helping to simulate and analyze potential outcomes based on concept interactions.
This repository provides access to the materials (code-data), software-environments (Jupyter Notebook), and the steps for reproducing the results for the project Modeling complex challenges utilizing insights from stakeholders and experts in heritage management: Novel methodologies in fuzzy cognitive mapping that focused on creating and analyzing Fuzzy Cognitive Maps (FCMs).

**The analysis includes three components: FCM Analysis focusing on Individual Heterogeneity, FCM aggregation, and the Collective FCM model's Structural and Influence Analysis.**

*The information below guides you through running the code. The main outputs are the CSV files, figures, and tables representing the results assessment of this project, located in the Analysis and output folders.*

### Concept Inventory:
- Generating an inventory of concepts and connections mentioned by stakeholders using CSV files.
- In this project, a list of terms based on the UNESCO factor list that influences the World Cultural Heritage Sites (WCHS) has been used.
- Standardized techniques were employed to merge similar concepts, and the results were presented in a table referred to as the Concept labels.CSV.

### Author: Amira.D (PhD Candidate at UT-ITC)

## Prerequisites

- Python 3.x installed on your computer
- Internet connection for downloading files
- Terminal (in Linux or MacOS), Powershell (Windows) command Line access

## Installing Python 3.x

### Windows

Python is **not** pre-installed on Windows, so you'll need to install it:

1. **Download Python:**
   - Visit [https://www.python.org/downloads/](https://www.python.org/downloads/)
   - Download the latest Python 3.x installer (Python 3.11 or newer recommended)

2. **Run the Installer:**
   - Double-click the downloaded `.exe` file
   - **Important:** Check the box **"Add Python to PATH"** at the bottom
   - Click "Install Now"

3. **Verify Installation:**
   - Open PowerShell or Command Prompt
   - Run: `python --version`
   - You should see something like `Python 3.11.x`

### macOS and Linux

Python 3 is **already pre-installed** on most modern macOS and Linux systems. To verify, run following command in your Terminal:
```bash
python3 --version
```

If Python 3 is not installed or you need a newer version:
- **macOS:** Download from [python.org](https://www.python.org/downloads/) or use Homebrew: `brew install python@3`
- **Linux:** Use your package manager (e.g., `sudo apt install python3 python3-pip python3-venv` on Ubuntu/Debian)

## Setup Instructions

1. Create a directory called `FCM`, preferably in your Desktop for easier finding.

2. Download the data and code files using the following links for [code](https://code.zip) and [data](https://-data.zip).

3. Extract both zip files and move them to `FCM` 

4. Download the `requirements.txt` from this repository file into your `swc-python` directory. Alternatively, create a `requirements.txt` file with the following content:

    ```
    numpy
    jupyterlab
    matplotlib
    ```

5. Open Terminal/Powershell into `swc-python` directory. Then, create a Python virtual environment:

    ```bash
    python -m venv venv
    ```

6. Activate the virtual environment:

    **On macOS/Linux:**
    ```bash
    source venv/bin/activate
    ```

    **On Windows:**
    ```cmd
    venv\Scripts\activate
    ```

    You should see `(venv)` appear at the beginning of your terminal prompt.

7. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

8. Launch Jupyter Lab:

    ```bash
    jupyter lab
    ```

    This will open Jupyter Lab in your default web browser. You're now ready to start coding!

## Verification

To verify your setup is correct, ensure:

- [ ] You are in the `swc-python` directory
- [ ] The virtual environment is activated (you see `(venv)` in your prompt)
- [ ] All packages are installed without errors
- [ ] Jupyter Lab opens in your browser

## Troubleshooting

### Python Command Not Found
If `python` doesn't work, try `python3` instead:
```bash
python3 -m venv venv
```

### Permission Issues
If you encounter permission errors during installation, ensure your virtual environment is activated.

### Jupyter Lab Won't Start
Make sure you've installed all packages from requirements.txt and your virtual environment is activated.

## Getting Help

If you encounter any issues during setup, please contact the author.

## Deactivating Virtual Environment

When you're done working, you can deactivate the virtual environment:

```bash
deactivate
```
## Dataset: Fuzzy cognitive maps

The dataset includes CSV spreadsheets that contain **matrixes detailing the number of concepts and their respective relationships**. 

**The data folder contains the 8 FCM files (CSV) used for the weight matrix and the concept labels file (CSV).**

### Data Format
The datasets are stored in comma-separated values (CSV) format. Each file represents a Fuzzy Cognitive Map (FCM) encoded as an adjacency matrix.
**In each matrix:**
- Rows and columns correspond to concepts within the FCM.
- The cell value at row i and column j represents the causal influence of concept i on concept j.

**Values are real numbers, where:**
- Positive values indicate a positive (reinforcing) causal relationship,
- Negative values indicate a negative (balancing) causal relationship,
- A value of 0 indicates no direct causal relationship between the two concepts.

*Diagonal elements are always zero, as self-loops are not considered.*

Each FCM matrix is square, meaning it has an equal number of rows and columns, corresponding to the total number of concepts included in that map. Concept labels (e.g., C1, C2, C3) are consistent across rows and columns to ensure interpretability and comparability.
**Example**
The adjacency matrix of FCM file is structured as follows:
```bash
        C2          C3          C1
C2   0.000000    0.610116    0.000000
C3   0.000000    0.541304    0.130328
C1  -0.722442    0.000000    0.000000

```
## Workflow
The overall workflow for the FCM analysis includes the following key steps:

**Exploring FCMs Properties:**
  - Input data, including the weight matrix and concept labels, are read from the Data folder. This includes files like EXPFCM(i).csv which contains the weight matrix of the FCM.
  - Notebook: 01 Exploring FCMs Properties.ipynb
**FCM Construction and Aggregation:**
  -The FCM is developed by employing the weight matrix of individual FCMs through qualitative and quantitative aggregation processes, resulting in the final merged FCM.
  -Notebook:02 FCM Construction and Aggregation.ipynb
**Collective FCM model's Structural and Influence Analysis**
  -
