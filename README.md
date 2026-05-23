# 📊 Analisis Sentimen: Pembatasan Akses Media Sosial untuk Anak di Bawah 16 Tahun

Proyek analisis sentimen terhadap komentar YouTube mengenai kebijakan pemerintah Indonesia yang membatasi akses media sosial dan game online untuk anak-anak di bawah 16 tahun.

## 📋 Deskripsi Proyek

Proyek ini menganalisis sentimen publik terhadap kebijakan Kementerian Komunikasi dan Digital (Komdigi) yang mulai berlaku pada 28 Maret 2026, yang melarang anak-anak di bawah 16 tahun untuk memiliki akun media sosial dan mengakses platform tertentu seperti Roblox.

### Tujuan
- Mengumpulkan opini publik dari komentar YouTube
- Menganalisis sentimen masyarakat (positif, negatif, netral)
- Memahami persepsi publik terhadap kebijakan pembatasan digital untuk anak

## 🗂️ Struktur Proyek

```
Submission 1-Analisis Sentimen/
├── README.md
├── .gitignore
├── .env
└── Submission Awal/
    ├── scraping.ipynb              # Notebook untuk scraping komentar YouTube
    ├── training.ipynb              # Notebook untuk preprocessing dan analisis sentimen
    ├── all_scraped_comments_final.csv  # Dataset komentar hasil scraping
    └── requirement.txt             # Dependencies Python
```

## 🚀 Cara Menggunakan

### 1. Clone Repository

```bash
git clone https://github.com/Adiwid20/underage-socmed-policy-analysis.git
cd underage-socmed-policy-analysis
```

### 2. Install Dependencies

```bash
pip install -r "Submission Awal/requirement.txt"
```

### 3. Setup Environment Variables

Buat file `.env` di root directory dan tambahkan kredensial API jika diperlukan:

```env
# Tambahkan API keys atau credentials di sini jika diperlukan
```

### 4. Jalankan Notebook

#### Scraping Data
Buka dan jalankan `Submission Awal/scraping.ipynb` untuk mengumpulkan komentar YouTube.

#### Analisis Sentimen
Buka dan jalankan `Submission Awal/training.ipynb` untuk:
- Preprocessing teks (cleaning, tokenization, stemming)
- Pelabelan sentimen menggunakan InSet Lexicon
- Analisis distribusi sentimen
- Visualisasi hasil

## 📊 Dataset

Dataset berisi **25,899 komentar** yang dikumpulkan dari **69 video YouTube** dengan topik terkait kebijakan pembatasan media sosial untuk anak.

### Kolom Dataset
- `platform`: Platform sumber (YouTube/YouTube Short)
- `video_id`: ID unik video
- `video_title`: Judul video
- `author`: Username pemberi komentar
- `comment`: Isi komentar
- `published_at`: Waktu publikasi komentar
- `reply`: Jumlah balasan
- `like_comment`: Jumlah like

## 🛠️ Teknologi yang Digunakan

### Libraries Utama
- **Data Processing**: pandas, numpy
- **Text Processing**: NLTK, Sastrawi
- **Visualization**: matplotlib, seaborn, wordcloud
- **Web Scraping**: google-api-python-client, selenium, playwright
- **Machine Learning**: scikit-learn, imbalanced-learn

### Tools
- Python 3.x
- Jupyter Notebook
- Git & GitHub

## 📈 Metodologi

1. **Data Collection**
   - Scraping komentar dari video YouTube terkait kebijakan
   - Filtering video yang relevan

2. **Data Preprocessing**
   - Cleaning teks (hapus URL, mention, emoji, dll)
   - Tokenization
   - Stopword removal
   - Stemming menggunakan Sastrawi

3. **Sentiment Labeling**
   - Pelabelan otomatis menggunakan InSet Lexicon
   - Klasifikasi: Positif, Negatif, Netral

4. **Analysis & Visualization**
   - Distribusi sentimen
   - Word cloud
   - Analisis temporal

## 📝 Hasil Analisis

> **Catatan**: Hasil analisis lengkap dapat dilihat di notebook `training.ipynb`

Dataset mencakup:
- ✅ 25,899 komentar total
- ✅ 69 video YouTube unik
- ✅ Data duplikat: 3,873 (sudah dibersihkan)
- ✅ Periode: 2021 - 2026

## 🤝 Kontribusi

Kontribusi, issues, dan feature requests sangat diterima! Silakan buat issue atau pull request.

## 📄 Lisensi

Proyek ini dibuat untuk keperluan pembelajaran dalam kursus **Belajar Fundamental Deep Learning** di Dicoding.

## 👤 Author

**Adiwid**
- GitHub: [@Adiwid20](https://github.com/Adiwid20)

## 🙏 Acknowledgments

- Dicoding Indonesia - Platform pembelajaran
- Kementerian Komunikasi dan Digital Indonesia - Sumber topik kebijakan
- YouTube API - Sumber data komentar

---

⭐ Jika proyek ini bermanfaat, jangan lupa berikan star!
