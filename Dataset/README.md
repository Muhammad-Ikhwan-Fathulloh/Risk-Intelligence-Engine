# 📊 Dataset Relevan untuk Risiko Kredit di Indonesia

Untuk membangun sistem **Risk Intelligence Engine** berbasis Graph AI dan LLM, berikut adalah beberapa dataset yang relevan dan dapat digunakan dalam konteks analisis risiko kredit korporasi:

---

## 1. ID-SMSA (Indonesian Stock Market Sentiment Analysis)

- **Deskripsi**: Dataset ini terdiri dari 3.288 tweet berbahasa Indonesia yang terkait dengan 10 perusahaan dengan kapitalisasi pasar terbesar di Indonesia. Sangat cocok untuk analisis sentimen pasar saham dalam konteks risiko investasi dan keuangan.
- **Kegunaan**: Analisis sentimen, deteksi emosi pasar, prediksi volatilitas saham.
- **Sumber**: [ScienceDirect - ID-SMSA Dataset](https://www.sciencedirect.com/science/article/pii/S2352340925003038)

---

## 2. Indonesian Financial Sentiment Analysis

- **Deskripsi**: Dataset ini tersedia di Hugging Face dan berisi data sentimen dalam bahasa Indonesia yang dikumpulkan dari berbagai sumber, khusus untuk domain keuangan.
- **Kegunaan**: Pelatihan model klasifikasi sentimen, integrasi dengan RAG dan LLM untuk penilaian risiko berbasis opini pasar.
- **Sumber**: [Hugging Face - Indonesian Financial Sentiment](https://huggingface.co/datasets/intanm/indonesian-financial-sentiment-analysis)

---

## 3. Credit Risk Dataset (Kaggle)

- **Deskripsi**: Dataset ini adalah simulasi data biro kredit yang mencakup berbagai fitur seperti pendapatan, riwayat pinjaman, durasi pinjaman, dan skor kredit. Sangat bermanfaat untuk membangun dan menguji model prediksi risiko kredit menggunakan machine learning.
- **Kegunaan**: Pelatihan model prediksi risiko kredit, evaluasi kinerja GNN dan model klasifikasi.
- **Sumber**: [Kaggle - Credit Risk Dataset](https://www.kaggle.com/datasets/laotse/credit-risk-dataset)

---

## 📌 Catatan

- Pastikan untuk membaca dan memahami lisensi penggunaan setiap dataset sebelum digunakan dalam proyek produksi atau komersial.
- Anda dapat menggabungkan dataset sentimen dengan dataset risiko kredit untuk membangun pipeline hybrid berbasis GNN + RAG + LLM guna mendukung pengambilan keputusan risiko yang lebih komprehensif.