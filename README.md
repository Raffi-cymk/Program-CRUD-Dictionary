# Program-CRUD-Dictionary
# Inisialisasi dictionary


![](<Program CRUD.jpeg>)


data_dict = {}
def print_menu():
    print("\nMenu Pilihan:")
    print("1. Lihat Data")
    print("2. Tambah Data")
    print("3. Ubah Data")
    print("4. Hapus Data")
    print("5. Cari Data")
    print("6. Keluar")
    
while True:
    print_menu()
    pilihan = input("Apa yang ingin Anda pilih? (1-6): ")

    if pilihan == '1':  # Lihat Data
        if data_dict:
            print("\nData yang Tersimpan:")
            for nim, data in data_dict.items():
                print(f"NIM: {nim}, Data: {data}")
        else:
            print("\nTidak ada data tersimpan.")

    elif pilihan == '2':  # Tambah Data
        nim = input("Masukkan NIM: ")
        if nim in data_dict:
            print("Data dengan NIM ini sudah ada.")
        else:
            data = input("Masukkan data: ")
            data_dict[nim] = data
            print("Data berhasil ditambahkan.")

    elif pilihan == '3':  # Ubah Data
        nim = input("Masukkan NIM yang ingin diubah: ")
        if nim in data_dict:
            data_baru = input("Masukkan data baru: ")
            data_dict[nim] = data_baru
            print("Data berhasil diubah.")
        else:
            print("Data dengan NIM ini tidak ditemukan.")

    elif pilihan == '4':  # Hapus Data
        nim = input("Masukkan NIM yang ingin dihapus: ")
        if nim in data_dict:
            del data_dict[nim]
            print("Data berhasil dihapus.")
        else:
            print("Data dengan NIM ini tidak ditemukan.")

    elif pilihan == '5':  # Cari Data
        nim = input("Masukkan NIM untuk mencari data: ")
        if nim in data_dict:
            print(f"Data ditemukan: {data_dict[nim]}")
        else:
            print("Data dengan NIM ini tidak ditemukan.")

    elif pilihan == '6':  # Keluar
        print("Keluar dari program.")
        break

    else:
        print("Pilihan tidak valid. Silakan coba lagi.")

---

# Penjelasan:
1. Inisialisasi: Program memulai dengan dictionary kosong (data_dict = {}).

2. Fungsi Menu: Fungsi print_menu() menampilkan daftar opsi yang sesuai dengan flowchart.

3. Operasi CRUD:
   
Lihat Data: Menampilkan isi dictionary.

Tambah Data: Menambahkan entri baru ke dictionary dengan NIM sebagai kunci.

Ubah Data: Mengganti nilai berdasarkan kunci tertentu.

Hapus Data: Menghapus entri berdasarkan NIM.

Cari Data: Mencari dan menampilkan data berdasarkan kunci.



4. Pengulangan: Program terus berjalan dalam loop hingga pengguna memilih untuk keluar (keluar).
        
