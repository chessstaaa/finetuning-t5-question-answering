# Fine-tuning T5-base for Generative Question Answering (SQuAD)

Proyek ini merupakan implementasi fine-tuning model **T5-base (Encoder–Decoder / Seq2Seq)** untuk tugas **Generative Question Answering** menggunakan dataset **SQuAD**.  
Model dilatih untuk menghasilkan jawaban teks langsung dari pasangan *question–context*.

---

## Identity
- Name: Darrell Chesta Adabi & Anom Nur Maulid
- Class: TK-46-01
- NIM: 1103223128 & 1103223193

---

## 📌 Project Overview

Pipeline end-to-end yang diimplementasikan:

1. Memuat dataset SQuAD
2. Mengonversi data QA ke format Seq2Seq T5  
   `question: <question> context: <context>` → `<answer>`
3. Fine-tuning model T5-base
4. Evaluasi menggunakan metrik SQuAD (Exact Match & F1)
5. Menyimpan metrik dan contoh hasil prediksi ke folder `reports/`

---

## ⚙️ Training Configuration

| Parameter | Value |
|----------|------|
| Dataset | rajpurkar/squad |
| Model | t5-base |
| Max source length | 384 |
| Max target length | 64 |
| Epochs | 1 |
| Learning rate | 0.0003 |
| Train batch size | 4 |
| Eval batch size | 4 |
| Gradient accumulation | 1 |
| Weight decay | 0.0 |

---

## 📊 Dataset Sizes

| Split | Samples |
|------|--------|
| Train | 87,599 |
| Validation | 10,570 |

---

## 📈 Evaluation Results (Validation)

| Metric | Value |
|-------|------|
| Eval Loss | 0.3899 |
| Exact Match (EM) | **68.40** |
| F1 Score | **82.18** |

---

## 🧠 Analysis

Model mampu menghasilkan jawaban teks yang cukup akurat hanya dengan 1 epoch fine-tuning.  
Nilai F1 yang tinggi menunjukkan bahwa model mampu menangkap konteks dan menghasilkan jawaban yang relevan meskipun Exact Match masih dapat ditingkatkan dengan training lebih lama atau hyperparameter tuning.

---

## 🗂 Repository Structure

- `notebooks/` : Notebook eksperimen dan training
- `reports/` : Hasil evaluasi dan contoh prediksi kualitatif (`qualitative_examples_squad.csv`)
- `requirements.txt` : Daftar dependency

---

## ▶️ How to Run

```bash
pip install -r requirements.txt
