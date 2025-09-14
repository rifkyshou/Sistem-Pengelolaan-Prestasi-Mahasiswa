# Sistem-Pengelolaan-Prestasi-Mahasiswa

## Identitas
- **Nama** : Awang Rifky Muhadzib  
- **Kelas** : B  
- **NIM** : 2509116059

## Deskripsi Program
Program ini dibuat untuk mengelola data prestasi mahasiswa dengan fitur:
1. Menambahkan prestasi mahasiswa.  
2. Melihat daftar prestasi mahasiswa.  
3. Keluar dari program.  

Data yang disimpan meliputi:
1. Nama Mahasiswa  
2. Nama Lomba  
3. Juara (1/2/3)  
4. Tahun Lomba  
5. Tingkat (Kabupaten/Provinsi/Nasional/Internasional)

## Flowchart Sistem Pengelolaan Prestasi Mahasiswa
<img width="788" height="1423" alt="Flowchart Mini Project Sistem Pengelolaan Prestasi Mahasiswa" src="https://github.com/user-attachments/assets/690b85ae-75a2-4902-9605-d19dd8aa08d5" />

## Penjelasan Flowchart Sistem Pengelolaan Prestasi Mahasiswa
### 1. Start
- Program dimulai dan menampilkan menu utama.

### 2. Tampilkan Menu Utama
- Program menampilkan 3 opsi:
1. Tambahkan Prestasi Mahasiswa
2. Lihat Daftar Prestasi Mahasiswa
3. Keluar dari Program

### 3. Input Nomor Menu
- Pengguna diminta memasukkan angka 1, 2, atau 3.
- Ini adalah **input** dari pengguna.

### 4. Validasi Pilihan Menu
- Program mengecek apakah input valid.
- Jika **tidak valid**, tampilkan pesan: "Pilihan tidak terdapat di menu, coba lagi."
- Setelah itu, kembali ke menu utama.

### 5. Jika Memilih `1` - Tambahkan Prestasi
- Program meminta pengguna mengisi data berikut:
  - Nama Mahasiswa
  - Nama Lomba
  - Juara ke-berapa (1/2/3)
  - Tahun Lomba
  - Tingkat Lomba (Kabupaten/Provinsi/Nasional/Internasional)
- Setelah semua data diinput:
  - Program menyimpan data ke list `data`.
  - Program menampilkan pesan: "Prestasi atas nama [nama] telah ditambahkan."
- Kembali ke menu utama.

### 6. Jika Memilih `2` - Lihat Prestasi
- Program mengecek apakah list `data` kosong.
  - Jika kosong, tampilkan: "Belum ada prestasi yang ditambahkan!"
  - Jika ada data, tampilkan seluruh daftar prestasi mahasiswa yang sudah disimpan.
- Setelah menampilkan, kembali ke menu utama.

### 7. Jika Memilih `3` - Keluar Program
- Program menampilkan pesan: "Terima kasih telah menggunakan sistem ini."
- Program berhenti dan flowchart berakhir di **End**.



## Program Sistem Pengelolaan Prestasi Mahasiswa
```python
# Mini Project Sistem Pengelolaan Prestasi Mahasiswa
# Nama : Awang Rifky Muhadzib
# Kelas : B
# NIM : 2509116059

data = []

while True:
    print("----------------------------------------------------------------------------------")
    print("         Menu Prestasi Mahasiswa     ")
    print("             pilih menu (1-5)           ")
    print("----------------------------------------------------------------------------------")
    print("1. Tambahkan Prestasi Mahasiswa")
    print("2. Lihat Prestasi Mahasiswa")
    print("3. Keluar")
    print("----------------------------------------------------------------------------------")

    daftar = input("Ingin Nomor Berapa? : ")

    if daftar == "1" :
        print("----------------------------------------------------------------------------------")
        print("     Tambahkan Prestasi Mahasiswa !     ")
        print("----------------------------------------------------------------------------------")
        nama = input("Nama Mahasiswa : ")
        lomba = input("Nama Lomba : ")
        juara = input("Juara Berapa 1/2/3 : ")
        tahun = input("Tahun Lomba : ")
        tingkat = input("Tingkat Kabupaten/Provinsi/Nasional/Internasional : ")

        data.append((nama, lomba, juara, tahun, tingkat))
        print("----------------------------------------------------------------------------------")
        print(f"    Prestasi Atas Nama {nama} Telah Ditambahkan !   ")
    
    elif daftar == "2" :
        print("----------------------------------------------------------------------------------")
        print("     Daftar Prestasi Mahasiswa")
        if data == [] :
            ("----------------------------------------------------------------------------------")
            print("         Belum ada Prestasi yang Ditambahkan !")
        else:
            n = 0
            while n < len(data) :
                a = data[n]
                print(f"{n+1}. {a[0]} - {a[1]} - Juara {a[2]} - Tahun {a[3]} - Tingkat {a[4]}")
                n = n + 1


    elif daftar == "3" :
        print("----------------------------------------------------------------------------------")
        print("     Terimakasih Telah Menggunakan   ")
        print(" Sistem Pengelolaann Prestasi Mahasiswa  ")
        print("----------------------------------------------------------------------------------")
        break


    else:
        print("----------------------------------------------------------------------------------")
        print("Pilihan tidak terdapat dimenu, Coba Lagi.")
```
## Kondisi

### Kondisi 1
<img width="402" height="210" alt="image" src="https://github.com/user-attachments/assets/82b97057-6f9b-4aaa-a118-b21f0ec2eb2a" />


- Fungsi: Menambahkan data prestasi baru ke dalam list data.
    - Program akan meminta pengguna mengisi:
    1. Nama mahasiswa
    2. Nama lomba
    3. Juara keberapa
    4. Tahun lomba
    5. Tingkat lomba
- Setelah diisi, data disimpan dan muncul pesan konfirmasi.
<img width="621" height="431" alt="image" src="https://github.com/user-attachments/assets/c57610b0-a04c-46f7-b32c-df9801573d65" />


Output ini menunjukkan bahwa data prestasi baru berhasil disimpan. Program tidak langsung berhenti, tapi kembali ke menu utama.

### Kondisi 2
<img width="347" height="206" alt="image" src="https://github.com/user-attachments/assets/37a1cace-2776-449d-9558-14e4efa0393f" />

Tujuan: Menampilkan semua data prestasi yang sudah tersimpan.

Pada Kondisi ini Memungkinkan Akan Ada Dua Output yang Berbeda
- JIka `data` Masing Kosong :
<img width="502" height="302" alt="image" src="https://github.com/user-attachments/assets/f8143ea4-dac1-4cd5-a069-9b7e667785a7" />

Program mengecek if data == [], karena kosong, ditampilkan pesan bahwa belum ada data prestasi.

- Jika `data` Sudah Diisi Setelah Menambahkan :
<img width="686" height="297" alt="image" src="https://github.com/user-attachments/assets/c1e7ba1c-83b8-426e-af2e-48e316058b85" />

Program melakukan looping while n < len(data) untuk menampilkan seluruh data prestasi yang sudah ditambahkan lengkap dengan urutan nomornya.





