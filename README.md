# finetuning-t5-question-answering

Fine-tuning **T5-base** (encoder–decoder / Seq2Seq) for **generative Question Answering** on **SQuAD**.

## Identity
- Name:
- Class:
- NIM:
- Group:

## Project overview
This repo contains an end-to-end pipeline:
1. Load SQuAD dataset
2. Convert QA examples into Seq2Seq format for T5 (`question: ... context: ...` → `answer`)
3. Fine-tune T5-base
4. Evaluate with SQuAD metrics (Exact Match & F1)
5. Save metrics + sample predictions to `reports/`

## Repository structure
- `notebooks/` : experiments and explanations
- `reports/` : final metrics and qualitative examples (tables/JSON)
- `requirements.txt` : dependencies

## How to run
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Open notebook:
   - `notebooks/01_t5_squad_qa.ipynb`

## Results
Fill in after training:
- Exact Match (EM):
- F1:
- Notes / error analysis:
