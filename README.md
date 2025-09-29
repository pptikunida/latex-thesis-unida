# latex-thesis-unida

![LaTeX](https://img.shields.io/badge/LaTeX-47862A?style=for-the-badge&logo=latex&logoColor=white)
![Engine](https://img.shields.io/badge/Engine-XeLaTeX-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Dikerjakan-yellow?style=for-the-badge)

---

## 🚀 Panduan Penggunaan & Alur Kerja

Panduan ini mencakup semua yang perlu kamu ketahui untuk menggunakan template ini secara efisien.

### 1. Manajemen Referensi dengan Zotero (Sangat Direkomendasikan)
Gunakan Zotero untuk manajemen referensi yang rapi dan otomatis.

**A. Setup (Hanya sekali di awal):**
1.  Install aplikasi [Zotero](https://www.zotero.org/) di komputermu.
2.  Install [Zotero Connector](https://www.zotero.org/download/connectors) untuk browser-mu.

**B. Alur Kerja:**
1.  **Simpan dari Web:** Saat menemukan sumber online, klik ikon Zotero di browser untuk menyimpannya.
2.  **Tambahkan `langid`:** Di aplikasi Zotero, pada *field* **`Extra`**, tambahkan baris `langid: indonesian` atau `langid: english`.
3.  **Export ke Proyek:** Di Zotero, pilih referensi -> klik kanan -> `Export Items...` -> pilih format `BibTeX` -> simpan sebagai `references.bib` di folder proyekmu.
4.  **Gunakan di Teks:** Kutip dengan `\footcite{kunci_referensi}`.

### 2. Konfigurasi TeXstudio (Setup Awal)
Atur TeXstudio-mu sekali saja agar proses kompilasi otomatis:
1.  Buka **`Options`** -> **`Configure TeXstudio...`** -> **`Build`**.
2.  **`Default Compiler`**: Pilih **`XeLaTeX`**.
3.  **`Default Bibliography Tool`**: Pilih **`Biber`**.

### 3. Alur Kerja Kompilasi & Git
* **Kompilasi:**
    * **Selalu *compile* dari file `main.tex`**.
    * Cukup tekan **`F5` (Build & View)** di TeXstudio untuk kompilasi lengkap.
* **Simpan ke GitHub/GitLab:**
    * Siklus 3 perintah di terminal: `git add .`, `git commit -m "Pesan perubahan"`, `git push`.

---

## 🛠️ Perangkat & Teknologi Utama
Proyek ini dibangun dan dikelola menggunakan serangkaian perangkat lunak dan paket LaTeX berikut:

### Aplikasi & Platform
* **Distribusi LaTeX:** MiKTeX
* **Editor:** TeXstudio
* **Manajemen Referensi:** Zotero
* **Version Control:** Git & GitHub/GitLab

### Engine & Paket LaTeX Kunci
* **Engine:** XeLaTeX
* **Sitasi:** `biblatex` (dengan `biber`)
* **Bahasa:** `polyglossia`
* **Layout Halaman:** `geometry`, `fancyhdr`, `titlesec`
* **Aset Visual:** `graphicx` (gambar), `booktabs` (tabel)
* **Daftar/List:** `enumitem`

---

## 📂 Struktur Folder Detail

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
├── 📄 main.tex (File utama)  
├── 📄 references.bib (Daftar pustaka)  
└── 📄 TEMPLATE.cls (Template yang digunakan)  

📄 .gitignore  
📄 README.md  

---  

## 🚀 Panduan Penggunaan umum

### 1. Cara Menambahkan Gambar
1.  **Simpan file gambar** (misal, `diagram.png`) ke dalam folder `assets/gambar/`.
2.  **Gunakan kode ini** di dalam file `.tex`-mu untuk menampilkannya:
    ```latex
    \begin{figure}[h!]
        \centering
        \includegraphics[width=0.8\textwidth]{assets/gambar/diagram.png}
        \caption{Keterangan untuk diagram ini.}
        \label{fig:diagram-sistem}
    \end{figure}
    ```
3.  **Rujuk gambar** di dalam teks dengan: `Gambar~\ref{fig:diagram-sistem}`.

### 2. Cara Menulis Daftar/List
Template ini sudah diatur agar daftar otomatis rapi.
* **Untuk Daftar Bernomor (1, 2, 3 lalu a, b, c):** Gunakan `enumerate`.
    ```latex
    \begin{enumerate}
        \item Poin utama pertama.
        \begin{enumerate}
            \item Sub-poin pertama.
        \end{enumerate}
    \end{enumerate}
    ```
* **Untuk Daftar *Bullet Point* (•):** Gunakan `itemize`.
    ```latex
    \begin{itemize}
        \item Poin pertama.
        \item Poin kedua.
    \end{itemize}
    ```

### 3. Cara Membuat Tabel
Gunakan `booktabs` untuk tabel yang bersih dan profesional.
1.  **Gunakan kode ini** sebagai cetak biru tabelmu:
    ```latex
    \begin{table}[h!]
        \centering
        \caption{Judul tabel di sini.}
        \label{tab:nama-unik-tabel}
        \begin{tabular}{lcc} % l=kiri, c=tengah, r=kanan
            \toprule
            Header 1 & Header 2 & Header 3 \\
            \midrule
            Data A1 & Data A2 & Data A3 \\
            \bottomrule
        \end{tabular}
    \end{table}
    ```
2.  **Rujuk tabel** di dalam teks dengan: `Tabel~\ref{tab:nama-unik-tabel}`.

### 4. Cara Menambah Referensi (Wajib Pakai Zotero)
1.  **Simpan ke Zotero:** Apapun sumbernya (Google Scholar, website jurnal, dll.), simpan referensi ke **Zotero** terlebih dahulu menggunakan **Zotero Connector** di browser.
2.  **Atur `langid`:** Di aplikasi Zotero, pada *field* **`Extra`**, tambahkan `langid: indonesian` atau `langid: english`.
3.  **Export ke Proyek:** Di Zotero, pilih referensi -> klik kanan -> `Export Items...` -> pilih format **`BibTeX`** -> simpan dan timpa file `references.bib` di folder proyekmu.
4.  **Gunakan di Teks:** Kutip di dalam tulisanmu menggunakan `\footcite{kunci_referensi_dari_zotero}`.

---

## ⚙️ Kompilasi & Konfigurasi
* **File Utama:** **Selalu *compile* dari file `main.tex`**.
* **Urutan Kompilasi Sakti:** Jika ada perubahan sitasi/referensi, jalankan urutan: **`XeLaTeX` → `Biber` → `XeLaTeX`**.
* **Pengguna TeXstudio:** Cukup tekan **`F5` (Build & View)**, dan urutan di atas akan berjalan otomatis jika sudah dikonfigurasi.

---

## 📈 Status Proyek
*Saat ini sedang dalam pengembangan struktur standarisasi teks*

---

## ✍️ Penulis
* **Muhammad Dafi Al Haq** - `452024611067` - `dafialhaq@student.cs.unida.gontor.ac.id`