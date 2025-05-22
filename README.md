# 🧠 Risk Intelligence Engine: Otomatisasi Analisis Risiko Kredit dengan GNN, RAG, dan LLM

Sistem ini bertujuan untuk mengotomatisasi analisis risiko kredit korporasi dengan pendekatan gabungan:
- **Graph Neural Network (GNN)** untuk representasi hubungan antar entitas.
- **Retrieval-Augmented Generation (RAG)** untuk menarik informasi kontekstual eksternal.
- **Large Language Model (LLM)** untuk reasoning berbasis Bahasa Indonesia.

---

# 📊 Dataset Relevan untuk Analisis Risiko Kredit di Indonesia

Untuk membangun sistem **Risk Intelligence Engine** berbasis **Graph Neural Network (GNN)**, **Retrieval-Augmented Generation (RAG)**, dan **Large Language Model (LLM)**, berikut adalah tiga dataset utama yang digunakan:

---

### 1. [ID-SMSA Dataset](https://github.com/Muhammad-Ikhwan-Fathulloh/Risk-Intelligence-Engine/blob/main/Dataset/IDSMSA.csv)

- **Deskripsi**: Dataset ini berisi 3.288 tweet berbahasa Indonesia terkait dengan 10 perusahaan dengan kapitalisasi pasar terbesar di Indonesia.
- **Fitur**:
  - `Tweet Date`
  - `Sentence`
  - `Quote Count`
  - `Reply Count`
  - `Retweet Count`
  - `Favorite Count`
  - `Sentiment`
  - `English Translation`
- **Kegunaan**: 
  - Analisis sentimen pasar terhadap perusahaan target secara real-time
  - Input tambahan untuk RAG dan LLM dalam menilai persepsi publik terhadap entitas keuangan
  - Deteksi anomali berbasis perubahan drastis sentimen

---

### 2. [Credit Risk Dataset](https://github.com/Muhammad-Ikhwan-Fathulloh/Risk-Intelligence-Engine/blob/main/Dataset/credit_risk_dataset.csv)

- **Deskripsi**: Dataset ini merupakan simulasi data biro kredit untuk keperluan pembelajaran dan riset.
- **Fitur**:
  - `person_age`
  - `person_income`
  - `person_home_ownership`
  - `person_emp_length`
  - `loan_intent`
  - `loan_grade`
  - `loan_amnt`
  - `loan_int_rate`
  - `loan_status`
  - `loan_percent_income`
  - `cb_person_default_on_file`
  - `cb_person_cred_hist_length`
- **Kegunaan**:
  - Prediksi risiko gagal bayar (default) nasabah atau korporat
  - Input utama untuk pemodelan GNN dan klasifikasi risiko
  - Membentuk relasi antar fitur untuk graph-based reasoning

---

### 3. [Indonesian Financial Sentiment Dataset (Hugging Face)](https://huggingface.co/datasets/intanm/indonesian-financial-sentiment-analysis)

```python
from datasets import load_dataset

# Load dataset sentimen keuangan Indonesia dari Hugging Face
ds = load_dataset("intanm/indonesian-financial-sentiment-analysis")
````

* **Deskripsi**: Dataset berisi kutipan teks keuangan dalam Bahasa Indonesia dan anotasi sentimen.
* **Fitur**:

  * `text`: kalimat atau paragraf berisi opini atau pernyataan finansial
  * `label`: anotasi sentimen (`positive`, `neutral`, `negative`)
* **Kegunaan**:

  * Melatih model klasifikasi sentimen keuangan berbasis Bahasa Indonesia
  * Dapat dipakai sebagai corpus retrieval untuk RAG
  * Kombinasi dengan ID-SMSA untuk memperluas cakupan sentimen pasar

---

## 🧩 Penggunaan Dataset dalam Sistem

| Dataset                         | GNN             | RAG                   | LLM |
| ------------------------------- | --------------- | --------------------- | --- |
| ID-SMSA                         | ❌               | ✅ (dokumen eksternal) | ✅   |
| Credit Risk                     | ✅ (node & edge) | ❌                     | ✅   |
| Sentimen Keuangan (HuggingFace) | ❌               | ✅                     | ✅   |

---

> 📌 **Tips**:
>
> * Gabungkan informasi dari ketiga dataset untuk membuat pipeline yang komprehensif: data tabular (risiko), teks sentimen (masukan publik), dan reasoning (LLM).
> * Cocok digunakan dalam aplikasi real-time monitoring atau scoring risiko berbasis AI.

---

Jika kamu ingin:
- Ekspor ke `.md` file
- Gabungkan ini ke README GitHub-mu
- Tambahkan visualisasi relasi antar dataset (GNN graph)

Bisa aku bantu sekarang juga!