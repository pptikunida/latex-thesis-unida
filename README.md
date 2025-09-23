# latex-thesis-unida

![LaTeX](https://img.shields.io/badge/LaTeX-47862A?style=for-the-badge&logo=latex&logoColor=white)
![Engine](https://img.shields.io/badge/Engine-XeLaTeX-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Dikerjakan-yellow?style=for-the-badge)

Repositori ini berisi semua file sumber LaTeX untuk penyusunan proposal skripsi dan skripsi sebagai syarat kelulusan Program Studi Teknik Informatika di Universitas Darrusalam Gontor.

---

## 📂 Struktur Proyek
Proyek ini disusun dengan struktur modular untuk kemudahan manajemen.

📁 THESIS/
├── 📁 assets/
│   ├── 📄 assets.tex
│   └── 🖼️ (dan gambar-gambar lainnya)
│
├── 📁 frontmatter/
│   ├── 📄 Abstract.tex
│   ├── 📄 Acknowledgements.tex
│   ├── 📄 authorization.tex
│   ├── 📄 cover.tex
│   └── 📄 Statement-Of-Originality.tex
│
├── 📁 mainmatter/
│   ├── 📄 chapter-1.tex
│   ├── 📄 chapter-2.tex
│   ├── 📄 chapter-3.tex
│   ├── 📄 chapter-4.tex
│   └── 📄 chapter-5.tex
│
├── 📄 main.tex (File utama)
├── 📄 references.bib (Daftar pustaka)
└── 📄 TEMPLATE.cls (Template yang digunakan)

📁 THESIS PROPOSAL/
├── 📁 assets/
│   ├── 📄 assets.tex
│   └── 🖼️ (dan gambar-gambar lainnya)
│
├── 📁 frontmatter/
│   ├── 📄 authorization.tex
│   └── 📄 cover.tex
│
├── 📁 mainmatter/
│   ├── 📄 chapter-1.tex
│   ├── 📄 chapter-2.tex
│   └── 📄 chapter-3.tex
│
├── 📄 .gitignore
├── 📄 main.tex (File utama)
├── 📄 README.md
├── 📄 references.bib (Daftar pustaka)
└── 📄 TEMPLATE.cls (Template yang digunakan)

---

## ⚙️ Cara Kompilasi
Pastikan kamu memiliki distribusi LaTeX yang modern seperti MiKTeX atau TeX Live.

1.  **Engine Wajib:** Proyek ini **wajib** dikompilasi menggunakan **XeLaTeX** karena menggunakan paket `fontspec` untuk manajemen font.
2.  **Rekomendasi Aplikasi** menggunakan TexStudio.
3.  **Urutan Kompilasi:** Untuk memastikan semua sitasi, referensi, dan daftar isi ter-update dengan benar, gunakan urutan kompilasi lengkap berikut:
    
    > **XeLaTeX → Biber → XeLaTeX → XeLaTeX**

---

## 🛠️ Teknologi & Paket Utama
Proyek ini dibangun menggunakan beberapa teknologi dan paket LaTeX utama, di antaranya:
* **Engine:** XeLaTeX
* **Distribusi:** MiKTeX
* **Sitasi:** BibLaTeX dengan style `chicago-notes`
* **Layout Judul:** `titlesec` & `titletoc`
* **Layout Halaman:** `geometry`
* **Daftar & List:** `enumitem`
* **Tabel Profesional:** `booktabs`
* **Manajemen Aset:** `graphicx` & `\newcommand`
* **Version Control:** Git & GitLab/GitHub

---

## 📈 Status Proyek
*Saat ini sedang dalam pengembangan struktur standarisasi teks*

---

## ✍️ Penulis
* **Muhammad Dafi Al Haq** - `452024611067` - `dafialhaq@student.cs.unida.gontor.ac.id`