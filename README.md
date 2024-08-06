
# Struktur Basis Data Proses Pelamar Kerja
![6](https://github.com/user-attachments/assets/2337acb7-c36d-4380-a630-622221185b3b)

# Entity Relationship Diagram (ERD) Penjelasan

ERD ini menggambarkan proses bagaimana data pelamar kerja diproses dan disalurkan ke perusahaan atau tempat kerja yang dilamar melalui platform penyedia layanan kerja online.

## Rancangan

### Entitas dan Atribut

1. **Pelamar Pekerjaan**
   - Atribut:
     - Nama pelamar
     - CV (Curriculum Vitae)
     - Ijazah
     - Transkrip

2. **Melamar Pekerjaan**

3. **Platform Penyedia Layanan Kerja Online**
   - Atribut:
     - Nama akun
     - Nomor ID
     - Biodata
     - Keahlian
     - Sertifikat pendukung
     - Pendidikan terakhir
     - Pengalaman kerja

4. **Menyalurkan Data Pelamar**

5. **Perusahaan/Tempat Kerja yang Dilamar**
   - Atribut:
     - Jenis pekerjaan
     - Status pekerjaan
     - Level pekerjaan
     - Persyaratan tertentu
     - Kualifikasi pekerjaan
     - Job description (deskripsi pekerjaan)

### Relasi

1. **Pelamar Pekerjaan → Melamar Pekerjaan**
   - **Relasi**: Satu pelamar pekerjaan bisa melamar ke beberapa pekerjaan.
   - **Tipe Relasi**: One-to-Many (satu-ke-banyak).

2. **Melamar Pekerjaan → Platform Penyedia Layanan Kerja Online**
   - **Relasi**: Proses melamar pekerjaan dilakukan melalui platform penyedia layanan kerja online.
   - **Tipe Relasi**: Many-to-One (banyak-ke-satu), karena banyak pelamar bisa menggunakan satu platform.

3. **Platform Penyedia Layanan Kerja Online → Menyalurkan Data Pelamar**
   - **Relasi**: Platform menyimpan dan menyalurkan data pelamar ke perusahaan.
   - **Tipe Relasi**: One-to-Many (satu-ke-banyak), karena satu platform bisa menyalurkan data banyak pelamar ke berbagai perusahaan.

4. **Menyalurkan Data Pelamar → Perusahaan/Tempat Kerja yang Dilamar**
   - **Relasi**: Data pelamar yang disalurkan oleh platform menuju ke perusahaan/tempat kerja yang dilamar.
   - **Tipe Relasi**: Many-to-One (banyak-ke-satu), karena banyak data pelamar bisa disalurkan ke satu perusahaan.

5. **Perusahaan/Tempat Kerja yang Dilamar**
   - **Relasi**: Perusahaan menyimpan informasi tentang berbagai aspek pekerjaan yang ditawarkan seperti jenis pekerjaan, status pekerjaan, level pekerjaan, persyaratan tertentu, kualifikasi pekerjaan, dan deskripsi pekerjaan.
   - **Tipe Relasi**: One-to-Many (satu-ke-banyak), karena satu perusahaan bisa memiliki banyak pekerjaan dengan berbagai persyaratan dan kualifikasi.

 Tujuan

1. **Efisiensi Pencarian Kerja**: Mempermudah pelamar pekerjaan untuk menemukan dan melamar pekerjaan yang sesuai dengan kualifikasi dan preferensi mereka melalui platform penyedia layanan kerja online.
   
2. **Manajemen Data**: Memastikan bahwa data pelamar dikelola dengan baik, termasuk informasi pribadi, pendidikan, pengalaman kerja, dan keahlian yang dimiliki.

3. **Penyaluran Data yang Tepat**: Memastikan data pelamar disalurkan dengan tepat ke perusahaan atau tempat kerja yang membutuhkan sesuai dengan jenis pekerjaan, kualifikasi, dan persyaratan yang ditetapkan.

4. **Optimalisasi Proses Rekrutmen**: Membantu perusahaan dalam proses rekrutmen dengan menyediakan data pelamar yang relevan dan sesuai dengan kriteria pekerjaan yang dibutuhkan.

5. **Transparansi dan Akurasi Informasi**: Menyediakan informasi yang akurat dan transparan tentang pekerjaan yang ditawarkan oleh perusahaan, termasuk deskripsi pekerjaan, status pekerjaan, level pekerjaan, dan persyaratan tertentu.

6. **Peningkatan Peluang Kerja**: Meningkatkan peluang kerja bagi pelamar dengan memperluas akses mereka ke berbagai lowongan pekerjaan melalui platform online.


Dengan laporan-laporan ini, kita dapat menganalisis data pelamar, proses lamaran, dan lowongan pekerjaan yang tersedia, sehingga dapat membantu dalam pengambilan keputusan yang lebih baik dalam proses rekrutmen.
