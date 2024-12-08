```mermaid
flowchart TD
    A[Mulai] --> B{Pilih Menu}
    B --> C[Tambah Data]
    B --> D[Tampilkan Data]
    B --> E[Hapus Data]
    B --> F[Ubah Data]
    B --> G[Keluar Program]

    C --> C1[Masukkan Nama dan Nilai]
    C1 --> C2[Tambahkan ke Daftar]
    C2 --> H[Kembali ke Menu]

    D --> D1{Apakah Data Kosong?}
    D1 -->|Ya| D2[Tampilkan Pesan: Belum Ada Data]
    D1 -->|Tidak| D3[Tampilkan Semua Data]
    D2 --> H
    D3 --> H

    E --> E1[Masukkan Nama]
    E1 --> E2{Nama Ditemukan?}
    E2 -->|Ya| E3[Hapus Data dari Daftar]
    E2 -->|Tidak| E4[Tampilkan Pesan: Nama Tidak Ditemukan]
    E3 --> H
    E4 --> H

    F --> F1[Masukkan Nama]
    F1 --> F2{Nama Ditemukan?}
    F2 -->|Ya| F3[Masukkan Nilai Baru]
    F3 --> F4[Perbarui Nilai di Daftar]
    F2 -->|Tidak| F5[Tampilkan Pesan: Nama Tidak Ditemukan]
    F4 --> H
    F5 --> H

    G --> I[Selesai]

    H --> B
