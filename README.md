
# Struktur Basis Data Proses Pelamar Kerja
![6](https://github.com/user-attachments/assets/2337acb7-c36d-4380-a630-622221185b3b)


ERD ini menggambarkan proses bagaimana data pelamar kerja diproses dan disalurkan ke perusahaan atau tempat kerja yang dilamar melalui platform penyedia layanan kerja online.

## Entitas dan Atribut

1. **Pelamar Pekerjaan**
   - Atribut:
     - Nama pelamar
     - CV (Curriculum Vitae)
     - Ijazah
     - Transkrip

 **Melamar Pekerjaan**

2. **Platform Penyedia Layanan Kerja Online**
   - Atribut:
     - Nama akun
     - Nomor ID
     - Biodata
     - Keahlian
     - Sertifikat pendukung
     - Pendidikan terakhir
     - Pengalaman kerja

 **Menyalurkan Data Pelamar**

3. **Perusahaan/Tempat Kerja yang Dilamar**
   - Atribut:
     - Jenis pekerjaan
     - Status pekerjaan
     - Level pekerjaan
     - Persyaratan tertentu
     - Kualifikasi pekerjaan
     - Job description (deskripsi pekerjaan)

## Relasi

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

## Garis Besar Relasi
- **One-to-Many**: Satu entitas di satu sisi bisa memiliki banyak entitas di sisi lainnya.
- **Many-to-One**: Banyak entitas di satu sisi bisa terhubung ke satu entitas di sisi lainnya.

Relasi-relasi dalam ERD ini menggambarkan alur pelamar yang memulai dengan data pribadi mereka, melamar pekerjaan melalui platform, dan akhirnya data mereka disalurkan ke perusahaan yang membutuhkan.
