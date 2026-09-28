# 🎵 A/B Testing Analysis: Personalized Playlist Recommendation System

## 📌 Executive Summary
Proyek ini bertujuan untuk menguji efektivitas intervensi kampanye personalisasi **"Rekomendasi Playlist Berdasarkan Mood Jam 8 Malam"** terhadap retensi dan perilaku pengguna aplikasi musik. Eksperimen dianalisis secara statistik untuk mengukur dampaknya terhadap durasi mendengarkan (*Duration Played*), tingkat keterlibatan (*Engagement Rate*), dan tingkat konversi pembayaran (*Payment Conversion Rate*).

---

## 🎯 Business Problem & Context
* **Latar Belakang**: Pengguna aktif pada jam istirahat malam (pukul 20:00) cenderung mengalami *decision fatigue* (kebingungan memilih lagu/playlist). Hal ini menyebabkan waktu dengar pengguna stagnan di rata-rata **120 menit/hari** dan menurunkan minat untuk beralih ke akun berbayar.
* **Solusi**: Memberikan intervensi berupa *push notification* dan kurasi khusus rekomendasi playlist jam 8 malam.

---

## 🔬 Experiment Setup & Hypothesis

### Groups:
* **Control Group**: Pengguna eksisting tanpa fitur rekomendasi jam 8 malam.
* **Target Group**: Pengguna yang menerima rekomendasi playlist berdasarkan mood jam 8 malam.

### Hypothesis Test:
* **$H_0$ (Hipotesis Nol)**: Tidak ada perbedaan signifikan pada *Duration Played*, *Engagement*, atau *Conversion Rate* antara grup Control dan Target.
* **$H_1$ (Hipotesis Alternatif)**: Grup Target memiliki *Duration Played*, *Engagement*, dan *Conversion Rate* yang lebih tinggi secara signifikan dibandingkan grup Control.

---

## 📊 Key Results & Findings

- **Duration Played**: Meningkat dari **120 menit** (Control) menjadi **159.79 menit** (Target) — bertambah **+40 menit** per hari.
- **Payment Conversion Rate**: Meningkat dari **69.9%** menjadi **79.86%** pada grup Target.
- **Statistical Significance**: Berdasarkan uji hipotesis statistik (*T-test* & *Chi-Square*), nilai **p-value < 0.05**. $H_0$ ditolak, membuktikan bahwa peningkatan ini signifikan secara statistik dan bukan karena kebetulan.

---

## 📈 Post-Implementation Trend Analysis
Setelah fitur dirilis secara bertahap selama 15 hari pasca-eksperimen:
1. **Minggu Pertama (1–7 Maret)**: Merupakan fase adaptasi algoritma dengan rata-rata **16,184 user/hari**.
2. **Minggu Kedua (8–15 Maret)**: Terjadi lonjakan adopsi pengguna hingga **+87.4% dalam sehari**, mencapai puncaknya di **29,803 user/hari** dan stabil di rentang **24,000–26,000 user/hari**.
3. **Pertumbuhan Total**: Volume pengguna meningkat sebesar **+52.26%** dari titik awal.

---

## 💡 Recommendations & Action Items

1. **Full Rollout**: Melakukan peluncuran fitur rekomendasi playlist jam 8 malam ke **100% seluruh pengguna** aplikasi.
2. **Retention Monitoring**: Memantau tingkat retensi pada minggu ke-3 dan ke-4 untuk memverifikasi bahwa lonjakan penggunaan bukan sekadar efek kejut sementara (*novelty effect*).
3. **Onboarding Enhancement**: Mengoptimalkan edukasi/komunikasi fitur pada hari pertama peluncuran untuk mengurangi periode adaptasi awal (*temporary dip*).

---

## 🛠️ Tools & Tech Stack
* **Python**: Data Processing & Hypothesis Testing (`scipy.stats`, `statsmodels`, `pandas`, `numpy`)
* **Visualization**: `matplotlib`, `seaborn`
* **Environment**: [Google Colab](https://colab.research.google.com/drive/1R4_vRibHYHgh8XROOYbLNchIgfgEk0VD#scrollTo=_IlwpIsRCKdw)
