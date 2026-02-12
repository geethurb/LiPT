# LiPT

LiPT is a Streamlit app for training a character-level GPT model on SMILES data and generating novel molecules.

## What It Does

- Upload a CSV file containing a `smiles` column.
- Train a GPT-based model on your uploaded molecules.
- Generate new candidate SMILES strings.
- Download generated molecules as CSV.
- Preview the first generated molecule structure in the app.

## Requirements

- Python 3.10+ recommended
- Dependencies from `requirements.txt`

## Setup

```bash
python -m venv .venv
```

### Windows (PowerShell)

```powershell
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

### macOS/Linux

```bash
source .venv/bin/activate
pip install -r requirements.txt
```

## Run

```bash
streamlit run app.py
```

Then open the URL shown in your terminal (usually `http://localhost:8501`).

## Input Format

Your uploaded CSV must include a column named:

- `smiles`

Example:

```csv
smiles
CCO
CC(=O)O
CCCC
```

## Notes

- Training time depends on dataset size and selected hyperparameters.
- GPU is used automatically if available; otherwise CPU mode is used.
