#  Sentiment Analysis with LLM on News Articles

Proyek ini bertujuan untuk melakukan analisis sentimen terhadap berita berbahasa Indonesia dan Inggris menggunakan model **LLM (Large Language Model)** dari OpenRouter API. Sistem ini mampu mendeteksi apakah suatu berita bernada **positif**, **netral**, atau **negatif**, beserta alasannya secara ringkas.

##  Fitur Utama

-  Input data berita berupa judul dan isi
-  Pembersihan teks otomatis (cleaning)
-  Stopword support Bahasa Indonesia (`Sastrawi`) & English (`nltk`)
-  LLM via OpenRouter (contoh model: `meta-llama/llama-4-scout`)
-  Output dalam format JSON (terstruktur)
-  Penanganan error parsing & fallback jika API gagal

##  Teknologi dan Library

- Python 3.8+
- [`requests`](https://pypi.org/project/requests/)
- [`nltk`](https://www.nltk.org/)
- [`sastrawi`](https://pypi.org/project/Sastrawi/)

##  Instalasi

1. Clone repository:

```bash
git clone https://github.com/Mzshine/Sentiment-Analysis-LLM.git
cd Sentiment-Analysis-LLM
```
##  Konfigurasi API
```
OPENROUTER_API_KEY = "sk-or-xxxxxxxx"
```
## Cara Penggunaan 
Masukan daftar berita dalam format berikut 
```
berita_list = [
    {"judul": "Ekonomi RI Tumbuh", "isi": "Ekonomi Indonesia tumbuh 5,2%..."},
    {"judul": "Cuaca Buruk Melanda", "isi": "Hujan deras menyebabkan banjir..."}
]
```
Lalu jalankan program, dan mendapatkan output dengan format JSON seperti berikut :
```
[
  {
    "judul": "Ekonomi RI Tumbuh",
    "isi": "Ekonomi Indonesia tumbuh 5,2%...",
    "sentiment": "positif",
    "reason": "Pertumbuhan ekonomi adalah indikator positif."
  },
  ...
]
```
