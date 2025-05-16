# EHR Data Cleansing Project

This project applies NLP and machine learning techniques to clean electronic health records (EHR) data. It standardizes medical terminology, corrects typos, and extracts medical entities.

## Folder Structure

- `data/` - Raw and processed datasets
- `notebooks/` - Jupyter notebooks for exploration and pipeline
- `utils/` - Utility functions for text cleaning
- `models/` - Placeholder for ML models (e.g., typo correction)
- `output/` - Cleaned and processed data outputs

## How to Run

1. Set up a Python environment and install dependencies:
```
pip install pandas spacy scispacy textblob nltk
pip install https://s3-us-west-2.amazonaws.com/ai2-s2-scispacy/releases/v0.4.0/en_core_sci_md-0.4.0.tar.gz
python -m textblob.download_corpora
```

2. Run Jupyter notebooks in the `notebooks/` folder step-by-step:
- `01_exploration.ipynb` - Load and explore data
- `02_cleaning_pipeline.ipynb` - Clean and correct typos

3. Extend further with medical entity recognition and standardization using scispaCy and UMLS (to be added).

## Dataset Sample

| patient_id | diagnosis_notes               | medications           |
|------------|------------------------------|----------------------|
| 1          | feverr and headeche           | paracetmol           |
| 2          | has diabates and hypertention | metformin, losartin  |
| 3          | dysnea with asthma            | salbutmol            |



## Additional Steps

### Step 3: Medical NER and UMLS Linking

- Use `scispaCy` models to extract medical entities and link them to UMLS codes.
- Run the notebook `03_medical_ner_umls.ipynb`.

### Step 4: ML-based Typo Correction and Standardization

- Use `TextBlob` for typo correction in diagnosis notes.
- Run the notebook `04_ml_standardization.ipynb`.

### Additional Dependencies

Make sure to install:

```
pip install textblob scispacy spacy
pip install https://s3-us-west-2.amazonaws.com/ai2-s2-scispacy/releases/v0.4.0/en_core_sci_md-0.4.0.tar.gz
python -m textblob.download_corpora
```

