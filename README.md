# patternrecognition-group1-groupexercise2
**Exercise 3 – Keyword Spotting (DTW)**

This repository contains our group solution for **Exercise 3** using **Dynamic Time Warping (DTW)** and sliding-window feature extraction.

This project uses **uv** for environment and dependency management.  
Install uv from: [https://docs.astral.sh/uv/getting-started/installation/](https://docs.astral.sh/uv/getting-started/installation/)

## Project Structure
```
exercise3-kws/
│
├── data/                     # dataset from ILIAS (NOT committed to repo)
│   ├── images/
│   ├── locations/
│   ├── train.tsv
│   ├── validation.tsv
│   ├── transcription.tsv
│   └── keywords.tsv
│
├── src/
│   ├── preprocess.py         # polygon extraction, cropping, binarization, normalization
│   ├── features.py           # sliding-window feature extraction
│   ├── dtw.py                # DTW distance computation
│   ├── retrieval.py          # keyword search + ranking
│   └── evaluation.py         # precision, recall, PR curves
│
├── main_ex3.py               # runs the full pipeline
├── notebooks/
│   └── exploration.ipynb
│
├── report.md                 # short report for submission
├── README.md                 # this file
│
│
├── .venv/                    # created automatically by uv sync (ignored by git)
├── .python-version           # created if uv pins Python version
├── uv.lock                   # dependency lockfile using pyproject.toml (created by uv)
├── pyproject.toml            # project + dependencies (replaces requirements.txt)
└── .gitignore                # ignores .venv, data, etc.
```

## Usage
1. Place the dataset inside `data/`.

2. Install dependencies using **uv**:
```
uv sync
```

3. Run the full pipeline with uv:
```
uv run main_ex3.py
```

## Notes
...
