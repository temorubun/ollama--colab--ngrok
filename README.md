# AI Chatbot UI (Streamlit + Ollama)

Aplikasi ini adalah chatbot berbasis web yang dibangun menggunakan Streamlit dan terhubung ke model AI melalui API (Ollama). Chatbot ini dapat menyimpan riwayat percakapan, memuat ulang chat sebelumnya, dan mendukung fitur download chat log.

## Fitur

- Chatbot interaktif berbasis web (Streamlit)
- Menyimpan dan memuat riwayat percakapan
- Download log percakapan
- Integrasi dengan model AI via API (Ollama)
- UI modern dan mudah digunakan

## Prasyarat

- Python 3.9 atau lebih baru
- Koneksi internet (untuk akses API Ollama)
- (Opsional) Docker, jika ingin menjalankan di container

## Instalasi

1. **Clone repository ini**
   ```bash
   git clone <repo-anda>
   cd Chat-ollama-UI-main
   ```

2. **(Opsional) Jalankan di Docker**
   ```bash
   docker run -it --network host -v ${PWD}:/app -w /app python:3.9 bash
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## Menjalankan Aplikasi

**JANGAN** jalankan dengan `python app.py`  
Gunakan perintah berikut agar Streamlit berjalan dengan benar:

```bash
streamlit run app.py
```

Setelah itu, buka browser dan akses alamat yang muncul, misal:  
- http://localhost:8501  
- atau alamat lain yang tertera di terminal

## Penggunaan

- Masukkan prompt/chat pada kolom input di bawah.
- Chatbot akan membalas secara interaktif.
- Untuk menyimpan riwayat chat, klik tombol **Save Chat** di sidebar.
- Untuk memuat chat sebelumnya, gunakan menu **Show/hide chat history** di sidebar.
- Untuk mengunduh log chat, klik **Download Chat Log** di sidebar.

## Struktur Folder

```
.
├── app.py                  # Source code utama aplikasi
├── requirements.txt        # Daftar dependensi Python
├── img.png                 # Contoh tampilan aplikasi
└── Intermediate-Chats/    # Folder penyimpanan riwayat chat
```

## Catatan

- Pastikan endpoint `ollama_url` di `app.py` sudah sesuai dengan API yang Anda gunakan.
- Jika menjalankan di Docker, pastikan port 8501 terbuka agar bisa diakses dari browser host.

## Contoh Tampilan

Lihat file `img.png` untuk contoh tampilan aplikasi chatbot. 