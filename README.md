# 📊 Analisis LRFM pada Nasabah Bank

Proyek ini bertujuan untuk menganalisis perilaku nasabah bank berdasarkan metrik **Length**, **Recency**, **Frequency**, dan **Monetary** (LRFM) menggunakan data terstruktur yang telah dibersihkan (`Banking_clean.csv`).

---

## 🎯 Tujuan

Memahami perilaku nasabah dan mengelompokkan mereka berdasarkan keterlibatan serta nilai ekonominya.  
Analisis ini dapat dimanfaatkan untuk:

- Strategi retensi pelanggan  
- Kampanye pemasaran yang lebih personal  
- Pengembangan program loyalitas  
- Mengurangi risiko churn (nasabah tidak aktif)

---

## 📁 Dataset

**Nama file:** `Banking_clean.csv`  
Dataset ini berisi informasi transaksi dan data nasabah yang telah dibersihkan.

### Kolom Penting (diasumsikan):
- `customer_id` — ID unik untuk setiap nasabah  
- `transaction_date` — Tanggal transaksi  
- `amount` — Nilai transaksi dalam mata uang lokal  
- `signup_date` — Tanggal nasabah mulai bergabung  

---

## 🔍 Definisi Metrik LRFM

| Metrik     | Deskripsi |
|------------|-----------|
| **Length (L)** | Rentang waktu antara transaksi pertama dan terakhir nasabah |
| **Recency (R)** | Waktu sejak transaksi terakhir hingga tanggal analisis |
| **Frequency (F)** | Jumlah transaksi yang dilakukan nasabah |
| **Monetary (M)** | Total nilai transaksi (pengeluaran) nasabah |

---

## 🛠️ Metodologi Analisis

1. **Pra-pemrosesan Data**
   - Konversi kolom tanggal ke format datetime
   - Menangani missing values
   - Mengelompokkan data berdasarkan `customer_id`

2. **Perhitungan Metrik LRFM**
   - `Length = last_transaction_date - first_transaction_date`
   - `Recency = snapshot_date_
