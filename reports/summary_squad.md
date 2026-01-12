# Task 2 — Fine-tuning T5-base for SQuAD (Generative QA)

Generated: 2026-01-11 07:57:53

## Setup
- Dataset: rajpurkar/squad
- Model: t5-base
- Max source length: 384
- Max target length: 64
- Epochs: 1
- Learning rate: 0.0003
- Train batch size: 4
- Eval batch size: 4
- Gradient accumulation: 1
- Weight decay: 0.0

## Data sizes used
- Train: 87599
- Validation: 10570

## Results (Validation)
| Metric | Value |
|---|---:|
| Eval loss | 0.3899 |
| Exact Match (EM) | 68.40 |
| F1 | 82.18 |

## Notes
- This is a **generative QA** setup using a T5-style input: `question: ... context: ...`
- For the training target, we used the **first** answer span in the SQuAD `answers["text"]` list.
- Qualitative examples saved to: `reports/qualitative_examples_squad.csv`
