# PEMOGRAMAN-11
# PROGRAM DAFTAR NILAI MAHASISWA

mahasiswa = {}     # struktur data: { "nama" : nilai }

# Fungsi menambah data mahasiswa
def tambah():
    nama = input("Masukkan nama: ")
    nilai = float(input("Masukkan nilai: "))
    mahasiswa[nama] = nilai
    print(f"Data {nama} berhasil ditambahkan.\n")

# Fungsi menampilkan seluruh data mahasiswa
def tampilkan():
    if not mahasiswa:
        print("Belum ada data.\n")
        return
    
    print("Daftar Nilai Mahasiswa:")
    for nama, nilai in mahasiswa.items():
        print(f"- {nama}: {nilai}")
    print()

# Fungsi menghapus data berdasarkan nama
def hapus(nama):
    if nama in mahasiswa:
        del mahasiswa[nama]
        print(f"Data {nama} berhasil dihapus.\n")
    else:
        print("Nama tidak ditemukan.\n")

# Fungsi mengubah data berdasarkan nama
def ubah(nama):
    if nama in mahasiswa:
        nilai_baru = float(input("Masukkan nilai baru: "))
        mahasiswa[nama] = nilai_baru
        print(f"Nilai {nama} berhasil diubah.\n")
    else:
        print("Nama tidak ditemukan.\n")


# PROGRAM UTAMA (opsional)
while True:
    print("=== MENU ===")
    print("1. Tambah Data")
    print("2. Tampilkan Data")
    print("3. Hapus Data")
    print("4. Ubah Data")
    print("5. Keluar")

    menu = input("Pilih menu: ")

    if menu == "1":
        tambah()
    elif menu == "2":
        tampilkan()
    elif menu == "3":
        nama = input("Masukkan nama yang ingin dihapus: ")
        hapus(nama)
    elif menu == "4":
        nama = input("Masukkan nama yang ingin diubah: ")
        ubah(nama)
    elif menu == "5":
        break
    else:
        print("Menu tidak valid.\n")


┌──────────────────────┐
          │        MULAI         │
          └──────────┬───────────┘
                     │
             ┌───────▼───────┐
             │   Tampilkan    │
             │     Menu       │
             └───────┬────────┘
                     │
            ┌────────▼────────┐
            │   Input Pilihan  │
            └────────┬────────┘
                     │
     ┌───────────────┼──────────────────────┐
     │               │                      │
 ┌───▼───┐       ┌───▼───┐             ┌────▼─────┐
 │Pilihan│       │Pilihan│             │Pilihan 3 │
 │   1   │       │   2   │             │ (Hapus)  │
 └───┬───┘       └───┬───┘             └────┬─────┘
     │               │                      │
┌────▼────┐    ┌─────▼────┐        ┌───────▼────────┐
│Tambah   │    │Tampilkan  │        │Input Nama yang  │
│Data     │    │   Data    │        │akan Dihapus     │
└────┬────┘    └─────┬────┘        └───────┬────────┘
     │               │                      │
     │               │              ┌───────▼────────┐
     │               │              │Hapus Data dari  │
     │               │              │   Dictionary    │
     │               │              └───────┬────────┘
     │               │                      │
     │               │                      │
     │               │                      │
     │               │                      │
     │               │                      │
     │               │                      │
     │               │                      │
     │               │                      │
     │               │                      │
     │               │                      │
   ┌─▼──────────┐ ┌──▼─────────────┐   ┌───▼───────────┐
   │Kembali ke   │ │Kembali ke Menu │   │Kembali ke Menu│
   │   Menu      │ │                │   │               │
   └─────────────┘ └───────────────┘   └───────────────┘
   ┌───────────────┐
             │ Pilihan 4 (Ubah)  
             └───────┬──────┘
                     │
             ┌───────▼─────────┐
             │Input Nama yang   │
             │     Diubah       │
             └───────┬──────────┘
                     │
             ┌───────▼─────────┐
             │Input Nilai Baru  │
             └───────┬──────────┘
                     │
             ┌───────▼─────────┐
             │Ubah Nilai dalam  │
             │   Dictionary     │
             └───────┬──────────┘
                     │
             ┌───────▼─────────┐
             │ Kembali ke Menu  │
             └──────────────────┘


             ┌──────────────┐
             │Pilihan 5     │
             │  (Keluar)    │
             └──────┬───────┘
                    │
            ┌───────▼───────┐
            │     SELESAI    │
            └───────────────┘
