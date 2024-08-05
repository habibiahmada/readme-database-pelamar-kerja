
# Struktur Basis Data Kafe
![Untitled Workspace](https://github.com/user-attachments/assets/ac925bad-7590-4fb2-91d5-75cfbf821328)

Basis data kafe ini memiliki beberapa tabel utama yang saling berhubungan. Setiap tabel memiliki Primary Key (PK) dan beberapa tabel memiliki Foreign Key (FK) yang mengacu ke tabel lain. Berikut adalah penjelasan detailnya.

## Tabel dan Atribut

### Pelanggan (Customer)
- **CustomerId** (PK): ID unik untuk setiap pelanggan.
- **FirstName**: Nama depan pelanggan.
- **LastName**: Nama belakang pelanggan.
- **Email**: Alamat email pelanggan.
- **Phone**: Nomor telepon pelanggan.

### Pegawai (Employee)
- **EmployeeId** (PK): ID unik untuk setiap pegawai.
- **FirstName**: Nama depan pegawai.
- **LastName**: Nama belakang pegawai.
- **Email**: Alamat email pegawai.
- **Phone**: Nomor telepon pegawai.
- **Title**: Jabatan pegawai.

### Kategori (Category)
- **CategoryId** (PK): ID unik untuk setiap kategori.
- **CategoryName**: Nama kategori produk.

### Produk (Product)
- **ProductId** (PK): ID unik untuk setiap produk.
- **ProductName**: Nama produk.
- **Price**: Harga produk.
- **CategoryId** (FK): ID kategori produk, mengacu ke tabel Kategori.

### Pembayaran (Payment)
- **PaymentId** (PK): ID unik untuk setiap pembayaran.
- **PaymentType**: Jenis pembayaran (misalnya, tunai, kartu kredit).
- **Amount**: Jumlah pembayaran.
- **PaymentDate**: Tanggal pembayaran.

### Pesanan (Order)
- **OrderId** (PK): ID unik untuk setiap pesanan.
- **OrderDate**: Tanggal pesanan.
- **CustomerId** (FK): ID pelanggan yang melakukan pesanan, mengacu ke tabel Pelanggan.
- **EmployeeId** (FK): ID pegawai yang menangani pesanan, mengacu ke tabel Pegawai.
- **PaymentId** (FK): ID pembayaran yang digunakan, mengacu ke tabel Pembayaran.

### Detail Pesanan (OrderDetail)
- **OrderDetailId** (PK): ID unik untuk setiap detail pesanan.
- **OrderId** (FK): ID pesanan, mengacu ke tabel Pesanan.
- **ProductId** (FK): ID produk yang dipesan, mengacu ke tabel Produk.
- **Quantity**: Jumlah produk yang dipesan.
- **Subtotal**: Total harga untuk jumlah produk yang dipesan.

## Relasi Antar Tabel

### Pelanggan ke Pesanan (Customer to Order) (1:M)
- **CustomerId** di tabel **Order** sebagai **FK** mengacu ke **CustomerId** di tabel **Customer** sebagai **PK**.
- Satu pelanggan dapat memiliki banyak pesanan, tapi satu pesanan hanya dapat dimiliki oleh satu pelanggan.

### Pegawai ke Pesanan (Employee to Order) (1:M)
- **EmployeeId** di tabel **Order** sebagai **FK** mengacu ke **EmployeeId** di tabel **Employee** sebagai **PK**.
- Satu pegawai dapat menangani banyak pesanan, tapi satu pesanan hanya dapat ditangani oleh satu pegawai.

### Kategori ke Produk (Category to Product) (1:M)
- **CategoryId** di tabel **Product** sebagai **FK** mengacu ke **CategoryId** di tabel **Category** sebagai **PK**.
- Satu kategori dapat memiliki banyak produk, tapi satu produk hanya dapat termasuk dalam satu kategori.

### Pesanan ke Detail Pesanan (Order to OrderDetail) (1:M)
- **OrderId** di tabel **OrderDetail** sebagai **FK** mengacu ke **OrderId** di tabel **Order** sebagai **PK**.
- Satu pesanan dapat memiliki banyak detail pesanan, tapi satu detail pesanan hanya terkait dengan satu pesanan.

### Produk ke Detail Pesanan (Product to OrderDetail) (1:M)
- **ProductId** di tabel **OrderDetail** sebagai **FK** mengacu ke **ProductId** di tabel **Product** sebagai **PK**.
- Satu produk bisa muncul di banyak detail pesanan, tapi satu detail pesanan hanya bisa memiliki satu produk.

### Pesanan ke Pembayaran (Order to Payment) (1:1)
- **PaymentId** di tabel **Order** sebagai **FK** mengacu ke **PaymentId** di tabel **Payment** sebagai **PK**.
- Satu pesanan hanya memiliki satu pembayaran, dan satu pembayaran hanya terkait dengan satu pesanan.

## Diagram ERD dalam Bentuk Teks

```plaintext
[ Pelanggan ]
- CustomerId (PK)
- FirstName
- LastName
- Email
- Phone

[ Pegawai ]
- EmployeeId (PK)
- FirstName
- LastName
- Email
- Phone
- Title

[ Kategori ]
- CategoryId (PK)
- CategoryName

[ Produk ]
- ProductId (PK)
- ProductName
- Price
- CategoryId (FK)

[ Pembayaran ]
- PaymentId (PK)
- PaymentType
- Amount
- PaymentDate

[ Pesanan ]
- OrderId (PK)
- OrderDate
- CustomerId (FK)
- EmployeeId (FK)
- PaymentId (FK)

[ DetailPesanan ]
- OrderDetailId (PK)
- OrderId (FK)
- ProductId (FK)
- Quantity
- Subtotal
```

Setiap entitas ditandai dengan Primary Key (PK) yang unik dan relasi antara entitas ditandai dengan Foreign Key (FK). Relasi ini menunjukkan bagaimana tabel-tabel tersebut saling berhubungan, memastikan integritas referensial dalam basis data.
```
```

Dokumen README ini memberikan penjelasan terstruktur tentang bagaimana tabel-tabel dalam basis data kafe saling berhubungan melalui Primary Key dan Foreign Key, serta menjelaskan atribut-atribut penting dalam setiap tabel.
