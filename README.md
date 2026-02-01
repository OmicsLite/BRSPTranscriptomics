# Study Case_OmicsLite_Week 3

## `Concept Workflow`
<img width="1341" height="475" alt="image" src="https://github.com/user-attachments/assets/a40e1c3b-9c56-46bb-bd59-5fdab9a98130" />

## Topic Week 3: Vaccine HIV
### Tools: GEO, GEO2R, R (R/Rstudio), GO (g:profiler), KEGG 
Ini adalah pembelajaran berbasis proyek (PBL) di OmicsLite tentang eksplorasi penjelasan dari satu jurnal tentang kasus HIV pada pasien DF, DHF, dan ND.

### Catatan: DF = Dengue Fever; DHF = Dengue Hemorrhagic Fever; ND: Non-Dengue (normal)

## Langkah-Langkah Analisis GEO / GEO2R
1. Periksa jurnal yang akan kita eksplorasi (hari ini tentang Vaksin HIV)
2. Periksa akses untuk GEO2R (terkadang beberapa dataset tidak dapat dieksplorasi secara publik, jadi kita tidak dapat menjalankannya di R) [Link GEO2R](<https://www.ncbi.nlm.nih.gov/geo/geo2r/>)
3. Setelah itu, periksa dataset (GSE18090), buka situs web analisis GEO2R
4. Di situs web analisis GEO2R, ​​kita dapat memfilter baris dan kemudian memberi nama, DF dan DHF sebagai "Pasien" dan ND sebagai "Normal"
5. Periksa opsi analisis di taskbar (di bawah)
6. Pilih "Opsi", Biasanya secara default opsi sudah dipilih. Tetapi, terapkan "Disediakan oleh Pengirim" di kategori platform (Karena NCBI mungkin menghasilkan beberapa perubahan pada dataset) dan pilih "ya" untuk menerapkan limma.
<img width="1764" height="541" alt="image" src="https://github.com/user-attachments/assets/031a9105-07a1-46ad-94bb-e399d739c3ff" />

7. Menjalankan data ("Reanalyze")
8. Kemudian, Anda dapat memilih visualisasi yang lebih baik, seperti plot heatmap dan diagram Venn, untuk DEG (Gen Ekspresi Diferensial)
9. Pilih "Unduh tabel", output akan menjadi "tsv"
10. Sebagai tantangan, Anda dapat mengkonversi data ekstensi .tsv menjadi .csv, kemudian mengkonversi dari data di Ms.Excel atau Anda dapat menggunakan basis data SQL. Tetapi dengan cara yang lebih mudah, Anda dapat menggunakan ChatGPT, untuk memfilter 20 gen sampel yang mengalami peningkatan dan penurunan ekspresi dalam dataset (dengan petunjuk)
11. Setelah mendapatkan 20 DEG yang mengalami penurunan ekspresi dan 20 DEG yang mengalami peningkatan ekspresi, Anda dapat menyalin "Gen Simbol". Biasanya, gen simbol memiliki dua atau lebih gen simbol dengan pembatas "//", Anda dapat menggunakan ChatGPT dengan perintah "Silakan, saring simbol "//" dalam data 20 DEG yang mengalami penurunan dan peningkatan ekspresi, setelah itu, buat data menjadi vertikal"


## Langkah-Langkah Analisis GO (Gene Ontology)
1. Kunjungi GO (situs web g:Profiler atau DAVID)
[Tautan g:Profiler](<https://biit.cs.ut.ee/gprofiler/gost>)
2. Masukkan daftar gen setelah penyaringan dan buat data vertikal (formulir ChatGPT)
3. Jalankan analisis
4. Kunjungi GO-BP, GO-MP, GO-CC. Temukan "Respons imun bawaan", "Respons inflamasi", "Respons terhadap virus", "Proses apoptosis", dll.
5. Jelajahi analisis lain untuk membuat kesimpulan.

## Langkah-Langkah KEGG Pathway
1. Identifikasi jalur hasil dari pengayaan.
2. Kunjungi KEGG Mapper [Link KEGG Mapper](<https://www.genome.jp/kegg/mapper/search.html>) (Cari organisme _Homo sapiens_)
3. Masukkan DEG (satu per satu), misalnya pertama masukkan DEG yang mengalami penurunan ekspresi kemudian analisis, setelah itu masukkan DEG yang mengalami peningkatan ekspresi
4. Analisis output (“Jalur pensinyalan reseptor Toll-like – 5 gen ditemukan”, “Interaksi sitokin-reseptor sitokin – 7 gen ditemukan”, “Apoptosis – 3 gen ditemukan”), gabungkan dengan hasil dari GO.

## Langkah-Langkah Interpretasi
1. Masukkan data visualisasi dari GEO2R (R/Rstudio)
2. Masukkan data daftar, seperti GO-BP, GO-MP, GO-CC.
3. Masukkan visualisasi data gen jalur.
4. Buat kesimpulan dengan visualisasi data tersebut.

Kamu tinggal eksplorasi dan pakai analisis mu dalam PBL OmicsLite
