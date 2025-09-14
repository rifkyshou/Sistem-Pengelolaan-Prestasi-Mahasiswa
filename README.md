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
<img width="347" height="203" alt="image" src="https://github.com/user-attachments/assets/f08b8445-93fb-4fc1-880e-7ba9d98d5778" />



- Fungsi: Menambahkan data prestasi baru ke dalam list data.
    - Program akan meminta pengguna mengisi:
    1. Nama mahasiswa
    2. Nama lomba
    3. Juara keberapa
    4. Tahun lomba
    5. Tingkat lomba
- Setelah diisi, data disimpan dan muncul pesan konfirmasi.
<img width="637" height="427" alt="image" src="https://github.com/user-attachments/assets/a075902a-542f-499a-bd7f-233f36bcc218" />

Output ini menunjukkan bahwa data prestasi baru berhasil disimpan. Program tidak langsung berhenti, tapi kembali ke menu utama.

### Kondisi 2
<img width="367" height="201" alt="image" src="https://github.com/user-attachments/assets/e42a5808-79c8-47b3-8990-a03f6ba9b15c" />

Tujuan: Menampilkan semua data prestasi yang sudah tersimpan.

Pada Kondisi ini Memungkinkan Akan Ada Dua Output yang Berbeda
- JIka `data` Masing Kosong :
<img width="486" height="293" alt="image" src="https://github.com/user-attachments/assets/f87aaff8-98a0-4862-9979-04a1ca998b59" />

Program mengecek if data == [], karena kosong, ditampilkan pesan bahwa belum ada data prestasi.

- Jika `data` Sudah Diisi Setelah Menambahkan :
<img width="740" height="297" alt="image" src="https://github.com/user-attachments/assets/b7c756c9-04e1-4078-ba0a-303ee155d31d" />


Program melakukan looping while n < len(data) untuk menampilkan seluruh data prestasi yang sudah ditambahkan lengkap dengan urutan nomornya.

### Kondisi 3

<img width="351" height="207" alt="image" src="https://github.com/user-attachments/assets/8f38d8a3-80b8-40ed-9d41-0045680d5584" />

Tujuan: Mengakhiri program.

<img width="376" height="273" alt="image" src="https://github.com/user-attachments/assets/65799938-a43c-4a93-996f-e1d742faa7b5" />

Setelah menampilkan pesan "Terimakasih Telah Menggunakan Sistem Pengelolaann Prestasi Mahasiswa ", program langsung menghentikan perulangan dengan break, sehingga program selesai berjalan.

### Kondisi 4
<img width="387" height="207" alt="image" src="https://github.com/user-attachments/assets/b37152f0-66f6-4295-9539-6d1849d201e8" />

Tujuan: input yang salah.

<img width="392" height="247" alt="image" src="https://github.com/user-attachments/assets/5330844e-cfc9-4490-8e64-077d3304834d" />

Karena input tidak cocok dengan angka 1, 2, atau 3, maka program menampilkan pesan "Pilihan tidak terdapat dimenu, Coba Lagi." dan langsung kembali ke menu utama.



