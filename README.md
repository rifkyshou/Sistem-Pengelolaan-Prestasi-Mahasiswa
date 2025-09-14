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

# Flowchart
<img width="788" height="1423" alt="Flowchart Mini Project Sistem Pengelolaan Prestasi Mahasiswa" src="https://github.com/user-attachments/assets/690b85ae-75a2-4902-9605-d19dd8aa08d5" />

# Program
```python
data = []

while True:
    print("----------------------------------------------------------------------------------")
    print("         Mwenu Prestasi Mahasiswa     ")
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
