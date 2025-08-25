# MolSearch - Molecular Similarity Search Pipeline

A robust molecular similarity search pipeline using RDKit and Streamlit, designed for cheminformatics and drug discovery applications.

## Features

- **Molecular Similarity Search**: Find similar molecules using Tanimoto coefficients
- **Molecular Featurization**: Convert molecules to feature vectors using RDKit descriptors
- **SQLite Database Storage**: Local database for molecule storage and retrieval
- **Streamlit Web Interface**: Interactive web application for molecular search

## Quick Start

### Live Demo
Try the live application: [MolSearch on Streamlit Cloud](https://molsearch.streamlit.app)

### Local Development
```bash
git clone https://github.com/rehanbchinoy/MolSearch.git
cd MolSearch
pip install -r requirements.txt
streamlit run app.py
```

## Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Query         │    │   Molecular     │    │   Similarity    │
│   Molecule      │    │   Featurizer    │    │   Search        │
└─────────┬───────┘    └─────────┬───────┘    └─────────┬───────┘
          │                      │                      │
          └──────────────────────┼──────────────────────┘
                                 │
                    ┌─────────────▼─────────────┐
                    │   SQLite Database         │
                    │   (Local Storage)         │
                    └─────────────┬─────────────┘
                                 │
                    ┌─────────────▼─────────────┐
                    │   Streamlit Interface     │
                    │   (Web UI)                │
                    └───────────────────────────┘
```

