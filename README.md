# Vision Transformer Model Comparison (DeiT vs Swin Transformer)

## Deskripsi Singkat
Repositori ini berisi implementasi dan eksperimen komparatif dua model Vision Transformer modern (DeiT dan Swin Transformer) untuk tugas klasifikasi citra sesuai tugas eksplorasi Deep Learning. Project bertujuan melakukan analisis performa, efisiensi model, serta trade-off antar-arsitektur dengan dataset kustom.

## Struktur Folder
```
.
├── dataset/
│   ├── train/
│   ├── test/
│   ├── train.csv
│   ├── test.csv
│   └── jawaban.csv
├── models/
│   └── *.pth (bobot model hasil training)
├── results/
│   ├── *.png (grafik/plot hasil)
│   ├── *.csv (tabel perbandingan)
│   └── summary_report.txt
├── main.ipynb (notebook utama)
├── requirements.txt
└── README.md
```

## Cara Menjalankan
1. **Clone repo ini dan masuk ke direktori project:**
   ```bash
   git clone https://github.com/dwiarthurrevangga/VisionTransformer-Comparison
   cd VisionTransformer-Comparison
   ```

2. **Siapkan environment Python (misal via conda):**
   ```bash
   conda create -n vit python=3.10
   conda activate vit
   ```

3. **Install dependensi:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Siapkan dataset:**
   - Taruh gambar sesuai struktur di folder `dataset/train/` (per subfolder kelas) dan `dataset/test/`.
   - Jika butuh, edit path di awal notebook agar sesuai dengan lokasi dataset Anda.

5. **Eksekusi notebook:**
   - Jalankan cell secara berurutan dari atas ke bawah (bisa pakai Jupyter Notebook, Colab, atau VSCode).
   - Semua output utama (plot, tabel, file jawaban.csv, dsb) akan otomatis tersimpan di dalam folder `results/` atau `dataset/jawaban.csv`.

## Penjelasan Kode
- **Eksperimen membandingkan:** DeiT-Small dan Swin-Tiny, keduanya di-finetuning pada dataset lokal, dievaluasi berbasis akurasi, precision, recall, F1, confusion matrix, waktu inferensi, dan ukuran model.
- **Notebook terpisah jadi banyak cell step-by-step:** mulai data loading, training, evaluasi, hingga komparasi metrik dan prediksi test-set.

## Output yang Dihasilkan
- Tabel perbandingan performa dan parameter dalam format csv/png
- Grafik learning curve dan confusion matrix
- File jawaban.csv untuk dataset test (hasil prediksi label final)
- Model weights terbaik tiap arsitektur (`*.pth`)

## Referensi
- [DeiT (Data-efficient Image Transformers) - Touvron et al., 2020](https://arxiv.org/abs/2012.12877)
- [Swin Transformer - Liu et al., 2021](https://arxiv.org/abs/2103.14030)
- [timm library repo](https://github.com/huggingface/pytorch-image-models)

## Kontak
- Nama: _Dwi Arthur Revangga_
- NIM: _122140144_
- Email: _dwi.122140144@student.itera.ac.id_