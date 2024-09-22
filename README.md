# Jarkom-Modul-1-IT42-2024

## Anggota

| Nama                      | NRP        |
| ------------------------- | ---------- |
| Muhammad Ida Bagus Rafi H      | 5027221059 |
| Naufal Syafi` Hakim      | 5027231022 |



# Laporan Resmi Modul 1

## 1. **Rizzset**
### **Tahap Pertama: Identifikasi Domain dan IP Address**
Langkah awal dimulai dengan mengidentifikasi domain dan IP yang terlihat jelas pada gambar berikut: ![image](https://github.com/user-attachments/assets/15543682-b57f-4941-9dcb-453774d53ae3). Dari gambar pertama, setelah memasukkan nama domain dengan format: `www.domain.com`. Nama domain yang dimaksud adalah **www.its.ac.id**, seperti yang terlihat dari *prompt* yang muncul di terminal. 

Selanjutnya, soal meminta untuk mengidentifikasi **IP address** dari domain tersebut. Peserta mencoba beberapa IP address seperti:

- 172.24.141.242
- 172.24.128.1
- 5.189.94.103

Namun, jawaban-jawaban tersebut salah. Akhirnya, IP address yang benar untuk domain **www.its.ac.id** adalah **103.94.189.5**, yang kemudian diterima sebagai jawaban benar.

 dari gambar pertama ini dapat disimpulkan Domain yang digunakan adalah www.its.ac.id, dan IP-nya sudah tercantum secara eksplisit, sehingga pertanyaan terkait domain dan IP berhasil terjawab.

 lalu sebelum melanjutkan ke tahap selanjutnya pertama lihat gambar dibawah ini :
![image](https://github.com/user-attachments/assets/82d3ce01-7674-49b7-bd9b-92c64cc3e289)

Dapat terlihat bahwa domain www.its.ac.id dan IP nya terpampang jelas sehingga 2 pertanyaan awal sudah solve (domain dan IP)

Untuk pertanyaan terkait JARM Fingerprint, sebuah repositori GitHub JARM di-*clone*, kemudian dijalankan dengan perintah `python jarm.py`. 

```bash
git clone https://github.com/salesforce/jarm
```

Setelah repositori selesai di-*clone*, peserta berpindah ke direktori **jarm** dengan perintah:

```bash
cd jarm/
```

Kemudian, dengan menjalankan perintah **python** di dalam direktori tersebut:

```bash
python jarm.py its.ac.id
```

Peserta berhasil memperoleh **JARM Fingerprint** dari domain **its.ac.id**. Hasil fingerprint yang dihasilkan adalah:

```
2ad2ad16d2ad2ad22c2ad2ad2ad2ad74aaecca9f9c4a3303863dfee62b241e
```

Fingerprint ini kemudian diinput ke dalam soal dan diterima sebagai jawaban yang benar. 

---

Hal ini menghasilkan string yang sesuai dengan yang diinginkan, yang terlihat dalam gambar berikut: ![image](https://github.com/user-attachments/assets/6ca3fc2f-d7f8-4fd8-923f-f916d695c82d). Dengan langkah tersebut, flagnya berhasil didapatkan.

### **Kesimpulan**
Challenge **Rizzset** menguji pemahaman tentang analisis DNS query, resolusi IP, dan penggunaan alat JARM untuk mendapatkan fingerprint dari server TLS. Langkah-langkah yang diikuti dalam challenge ini meliputi:

1. Menemukan nama domain yang diminta dari *DNS query*.
2. Menemukan IP address dari domain tersebut.
3. Menggunakan JARM untuk mendapatkan fingerprint dari server TLS yang sesuai dengan domain yang dianalisis.
4. Memasukkan hasil fingerprint sebagai jawaban untuk menyelesaikan soal.

Gambar-gambar yang disertakan di setiap langkah memberikan bukti visual tentang proses yang dilakukan selama penyelesaian challenge.

## 2. **EZ**
### **Langkah 1: Mengidentifikasi Pesan Petunjuk**
Pada gambar pertama, ditemukan sebuah pesan yang menjadi kunci awal dalam challenge ini. Pesan ini berisi instruksi untuk peserta, di mana terlihat pesan yang ditulis sebagai berikut:

```
pesan: "jawabannya jawaban"
itu ya yg disubmit yang ada e.petiknya
```

Pesan ini memberikan informasi langsung bahwa jawaban yang harus dimasukkan adalah "jawabannya jawaban", lengkap dengan tanda kutipnya. Petunjuk ini mempermudah peserta dalam mengetahui apa yang harus dikirimkan untuk menyelesaikan bagian pertama dari tantangan.  
![Gambar Pertama](https://github.com/user-attachments/assets/22544583-fc88-4d3a-8d4b-17f086fa91f5)

### **Langkah 2: Menganalisis Source dan Destination Address**
Pada gambar kedua, terdapat rincian tentang komunikasi jaringan yang menunjukkan informasi penting mengenai alamat IP sumber dan tujuan, serta nomor port yang digunakan. Berikut adalah detail dari paket tersebut:

- **Source Address**: 172.24.128.1
- **Destination Address**: 172.24.141.242
- **Source Port**: 36199
- **Destination Port**: 1234

Analisis paket ini menunjukkan bahwa port 1234 digunakan sebagai *destination port* untuk layanan tersebut. Petunjuk ini sejalan dengan informasi yang harus dicari oleh peserta, yaitu nomor port yang digunakan oleh layanan yang terkait dengan tantangan ini.  
![Gambar Kedua](https://github.com/user-attachments/assets/6b718f90-d9c5-4c3f-b54f-d042ebbd59d0)


## **Langkah 3: Menggunakan Netcat untuk Menemukan Flag**
Pada gambar ketiga, terlihat bahwa peserta menggunakan perintah *netcat* untuk terhubung ke alamat IP dan port yang relevan dalam tantangan ini. Peserta menjalankan perintah berikut:

```
netcat 10.15.42.60 54000
```

Setelah terhubung, terdapat serangkaian instruksi yang meminta peserta untuk menemukan jawaban dari log yang diberikan. Peserta diminta untuk memasukkan jawaban sesuai dengan format yang diberikan, yaitu sebuah string. Dengan menggunakan petunjuk dari langkah pertama, peserta memasukkan jawaban "jawabannya jawaban", dan akhirnya sistem mengonfirmasi bahwa jawaban tersebut benar.  
![Gambar Ketiga](https://github.com/user-attachments/assets/d528b2d7-1c59-4c3d-802f-547dc9b94a07)

### **Langkah 4: Mendapatkan Flag**
Setelah jawaban benar dimasukkan, sistem memberikan flag sebagai hasil akhir dari tantangan ini. Berikut adalah flag yang diperoleh peserta:

```
JarkomITíBiAr_aman_Pake_sSh_micIxpdbrdn7PcyzOSYUsy7ot3zV5xLU7XJncyv4EFKd7WISM8FPEZ
```

### **Kesimpulan**
Dalam penyelesaian challenge **EZ**, peserta berhasil mengidentifikasi string jawaban dengan menganalisis pesan-pesan yang ditemukan di dalam log. Selain itu, informasi tentang *destination port* (1234) juga diperoleh dari hasil analisis paket jaringan. Pada akhirnya, dengan menggunakan *netcat* untuk terhubung ke server dan memasukkan jawaban yang benar, peserta berhasil mendapatkan flag yang diperlukan untuk menyelesaikan tantangan.

### 3. **FTPLOGIN**
Pada soal ini, metode *bruteforce* digunakan untuk mendapatkan informasi login yang berhasil. Hal ini dilakukan dengan mengikuti *stream* yang menunjukkan keberhasilan login, seperti ditampilkan pada gambar berikut: ![image](https://github.com/user-attachments/assets/5e3bca6b-2486-4f5b-b2d7-a04902d43f97). Tampilan terminal dari proses ini dapat dilihat pada gambar berikut: ![Screenshot 2024-09-19 002340](https://github.com/user-attachments/assets/52b32f3f-e61c-4e74-938b-b276c6f7fe66).



## 4. **Advance Sanity Check**
Untuk challenge ini, hal yang perlu dilakukan adalah mengikuti *stream* data untuk menemukan informasi penting. Dalam gambar pertama, terlihat username dan nama file yang dicari. untuk menyelesaikan challange ini adalah melakukan langkah-langkah berikut:

1. **Mengidentifikasi Data**: Melihat *stream* dan menemukan bagian yang mencantumkan username dan nama file.  Diharuskan teliti dalam mencatat informasi ini untuk langkah selanjutnya.
   
   Gambar yang relevan: ![image](https://github.com/user-attachments/assets/2b6ceded-e16a-467c-93b2-9d9864bcb0cf) dan ![Screenshot 2024-09-19 003336](https://github.com/user-attachments/assets/7df020ca-9315-40c2-a4a4-a36a05137ce8).

2. **Melakukan Dekripsi**: Setelah mengidentifikasi username dan file, peserta melakukan dekripsi untuk mendapatkan informasi lebih lanjut. Dekripsi ini dapat mencakup penggunaan tool tertentu atau metode manual yang sesuai.

   Gambar terminal proses dekripsi: ![image](https://github.com/user-attachments/assets/b2aee3ea-fca7-4c88-8e61-2ac3f29d44f8).

---

## 5. **Pegawai Negeri Sebelah**
Dalam challenge ini, informasi mengenai *password*, *jabatan*, dan *username* sangat penting. Hal yang harus dilakukan untuk menyelesaikan challange ini adalah, mengikuti langkah-langkah berikut:

1. **Analisis Stream**: Mengikuti *stream* dan menemukan string yang berisi *password*, *jabatan*, dan *username*. Diharus mencari bagian yang tepat dan menyalin informasi ini.

   Tampilan terminal menunjukkan hasil analisis: ![image](https://github.com/user-attachments/assets/6b97126b-7e3a-483b-a007-8aab87e087c5).

2. **Verifikasi Data**: Memastikan bahwa data yang ditemukan sesuai dengan pertanyaan yang diajukan, sehingga yakin informasi tersebut relevan dan akurat.

---

## 6. **Malicious Code**
Pada challange ini hal yang diharuskan untuk menganalisis traffic dan mengidentifikasi pola serangan. Berikut langkah-langkah yang diambil:

1. **Menghitung Directory Listing**:  menghitung jumlah trafik GET yang berfungsi sebagai *directory listing*. Dalam gambar terlihat bahwa totalnya adalah 52.

   Gambar analisis trafik GET: ![image](https://github.com/user-attachments/assets/083d716e-ee48-4737-82fb-f3630152583d).

2. **Identifikasi Endpoint Login**: Dalam *stream* yang diikuti, menemukan endpoint login `/index.php`. Ini menjadi informasi kunci untuk menganalisis serangan lebih lanjut.

   Gambar endpoint login: ![image](https://github.com/user-attachments/assets/7906fb43-fb63-4253-9826-7c54d6ec2f0f).

3. **Menghitung Bruteforce Attempts**:  menghitung jumlah *stream* yang terjadi setelah *directory listing*. Setelah mengidentifikasi bahwa ada 207 *stream* untuk email jarkom, peserta dapat menghitung total *stream* sebelum *bruteforce* yang terjadi, yaitu 153.

   Gambar analisis *stream*: ![image](https://github.com/user-attachments/assets/c3d032b6-f9bb-4752-963e-77cbcb6fc121).

---

## 7. **Corporate Breach**
Challenge ini berhubungan dengan informasi yang ditemukan di challenge sebelumnya. Berikut langkah-langkahnya:

1. **Menggunakan Informasi Sebelumnya**: mengambil username jarkom yang sudah ditemukan sebelumnya dan menerapkannya untuk menjawab pertanyaan dalam challenge ini.

2. **Verifikasi**: Pastikan bahwa semua informasi yang digunakan sesuai dengan konteks yang diberikan dan menjawab semua pertanyaan dengan benar.

---

## 8. **Surprise**
pada challange ini perlu menemukan IP dan informasi lainnya dalam challenge ini. Langkah-langkah yang diambil meliputi:

1. **Menelusuri IP**: Menggunakan gambar untuk menemukan IP yang relevan,  diharus teliti dalam meninjau semua detail yang ada.

   Gambar pencarian IP: ![image](https://github.com/user-attachments/assets/7903d35f-fe25-400e-b2a5-5b17a1c0444c).

2. **Mencari Pesan Penyerang**: Dengan menggunakan *prompt* dari ChatGPT untuk mendapatkan informasi tentang pesan yang ditinggalkan oleh penyerang, yang mengungkapkan warna favorit pembuat tantangan.

   Gambar terminal hasil: ![image](https://github.com/user-attachments/assets/9b0ad277-ccbb-4fc2-acfb-2f2850fc4738).

---

## 9. **Illegal Breakthrough**
pada challane ini perlu mengidentifikasi berbagai elemen penting. Langkah-langkahnya meliputi:

1. **Identifikasi Tools dan Endpoint**: Melihat terminal yang menunjukkan informasi terkait username, tools yang digunakan, dan endpoint yang terlibat dalam serangan.

   Gambar terminal: ![image](https://github.com/user-attachments/assets/a50f8b81-51e0-4ece-b1cf-5d9e200cf23d).

2. **Mencari IP dan Port**: Gambar lainnya memberikan informasi tentang IP dan port yang digunakan dalam serangan, yang sangat penting untuk analisis.

   Gambar IP dan port: ![image](https://github.com/user-attachments/assets/044c26f4-7327-4425-b5d1-a6bce5a4422e).

---

## 10. **Packet Barrage**
Challenge ini mengharuskan untuk menyelesaikannya dihadapi dengan keterbatasan waktu. Langkah-langkah yang diambil meliputi:

1. **Mencari File Malware**: harus mencari file malware dan nama file yang relevan dalam gambar yang disediakan.

   Gambar file malware: ![image](https://github.com/user-attachments/assets/88bd9bfd-cca6-49f3-a7b1-47b37e2beb31).

2. **Identifikasi Alamat IP**: Menggunakan gambar untuk menemukan alamat IP yang terkait dengan malware tersebut.

   Gambar alamat IP: ![image](https://github.com/user-attachments/assets/08635d8d-6281-462d-92c7-478256479776).

3. **Menghitung Total Bruteforce**: Menghitung jumlah total *bruteforce* dengan cara mengurangi satu dari total angka *stream* yang ada, menghasilkan 1917.

   Gambar analisis *stream*: ![image](https://github.com/user-attachments/assets/b516c05a-0237-493f-b8f7-3ebdd2ceca6c).

---










---
# written jarkom-modul-1-IT42-2024

# Langsung saja ini adalah write-up nya
# Naufal Syafi' Hakim [5027231022]
# M.Ida Bagus Rafi .H. [50272210xx]
## Rizzset 
Begini kira-kira saya mendapatkan flag
![image](https://github.com/user-attachments/assets/15543682-b57f-4941-9dcb-453774d53ae3)
Oke jadi pertama kita lihat gambar dibawah ini :
![image](https://github.com/user-attachments/assets/82d3ce01-7674-49b7-bd9b-92c64cc3e289)

Dapat terlihat bahwa domain www.its.ac.id dan IP nya terpampang jelas sehingga 2 pertanyaan awal sudah solve (domain dan IP)
Selanjutnya untuk pertanyaan JARM Fingerprint saya mengclone github JARM sendiri lalu masukkan ke folder local saya dan saya mengetikan python jarm.py untuk mendapatkan string yang diinginkan. Kira-kira begini :
![image](https://github.com/user-attachments/assets/6ca3fc2f-d7f8-4fd8-923f-f916d695c82d)
Setelah itu sudah mendapatkan flagnya.

## EZ
Pertama membuka wireshark saya langsung follow salah satu baris dan mencari-cari clue dan menemukan ini :
![Screenshot 2024-09-19 001621](https://github.com/user-attachments/assets/22544583-fc88-4d3a-8d4b-17f086fa91f5)
clue nya adalah string "jawabannya jawaban". Lalu selanjutnya terdapat clue Destination Port pada paket seperti ini 
![image](https://github.com/user-attachments/assets/6b718f90-d9c5-4c3f-b54f-d042ebbd59d0)
Maka dari ini saya mendapatkan flagnya, kira-kira beginilah terminalnya 
![image](https://github.com/user-attachments/assets/d528b2d7-1c59-4c3d-802f-547dc9b94a07)

## FTPLOGIN
Pada ftplogin begini terminal saya :
![Screenshot 2024-09-19 002340](https://github.com/user-attachments/assets/52b32f3f-e61c-4e74-938b-b276c6f7fe66)
Caranya adalah dengan bruteforce mencari follow stream yang memiliki login successfull
![image](https://github.com/user-attachments/assets/5e3bca6b-2486-4f5b-b2d7-a04902d43f97)

## Advance Sanity Check
Begini terminal saya
![image](https://github.com/user-attachments/assets/e04cc264-4898-4784-8578-324e955bf0e9)
Username?
![image](https://github.com/user-attachments/assets/2b6ceded-e16a-467c-93b2-9d9864bcb0cf)
Filename?
![Screenshot 2024-09-19 003336](https://github.com/user-attachments/assets/7df020ca-9315-40c2-a4a4-a36a05137ce8)
Bagaimana saya menemukannya ya follow stream lait-liat aja yang lain.

Cara mendecodenya saya seperti ini
![image](https://github.com/user-attachments/assets/b2aee3ea-fca7-4c88-8e61-2ac3f29d44f8)

## Pegawai Negeri Sebelah
Pada salah satu stream saya menemukan ini :
![image](https://github.com/user-attachments/assets/042213f2-ff28-415d-9f02-70d59a30875e)
Pada stream tersebut semua informasi(passwd,Jabatan,username awal,password akhir) yang ditanyakan oleh soal sudah terjawab semua sehingga saya sepertinya tidak perlu mensreeshootnya satu satu karena memakan waktu
Beginilah terminalnya :
![image](https://github.com/user-attachments/assets/6b97126b-7e3a-483b-a007-8aab87e087c5)

## Malicious Code
Disini ditanyakan berapa kali attacker melakukan directory listing yang artinya kita menghitung berapa kali traffic GET muncul terlihat terdapat 52
![image](https://github.com/user-attachments/assets/083d716e-ee48-4737-82fb-f3630152583d)
Lalu untuk endpoint apa untuk login ya tentu saja bisa kita lihat pada stream yang attacker bruteforce pada login page, terdapat endpoint /index.php
![image](https://github.com/user-attachments/assets/7906fb43-fb63-4253-9826-7c54d6ec2f0f)
Lalu untuk pertanyaan berapa kali attacker melakukan bruteforce, kita bisa menghitung berapa stream yang terjadi setelah attacker melakukan data listing dan sebelum attacker masuk ke dalam sistem. Menghitungnya begini, stream pada email jarkom adalah 207 maka stream setelah itu tidak dihitung, lalu dikurangi dengan stream sebelum attacker melakukan bruteforce hasilnya adalah 153 
Ini adalah bukti stream email jarkom :
![image](https://github.com/user-attachments/assets/c3d032b6-f9bb-4752-963e-77cbcb6fc121)

Lalu untuk pertanyaan dari attacker saat ditranslate ChatGPT adalah "apa warma favorit pencbuat challenge his tweaten ter)"
![image](https://github.com/user-attachments/assets/a8e0c10d-49a3-4a9d-a665-d3b6d0a85d06)
Ya! mas nevarre suka warna merah tentu saya tahu.
Begini tampilan terminal saya :
![image](https://github.com/user-attachments/assets/9b0ad277-ccbb-4fc2-acfb-2f2850fc4738)
Ya banyak sekali bruteforce takmuat dalam satu foto saja

## Corporate breach
![image](https://github.com/user-attachments/assets/41bb3c20-e92d-4424-af23-c659ac707c56)
Soal ini sebenarnya adlah soal sebelumnya dari Malicious Code jadi tentu saya sudah mengerjakan corporate breach terlebih dahulu, bisa dilihat saya menemukan username jarkom di foto write-up pada malicius code sehingga saaya tidak perlu menguploadnya lagi

## Surprise
![image](https://github.com/user-attachments/assets/d33a3ce9-de59-4e99-bd8f-0cd31cbac105)
Pada surprise ini saya akan jelaskan karena ini adalah lanjutan dari ftp login, bagaimana saya menemukan ip?
![image](https://github.com/user-attachments/assets/7903d35f-fe25-400e-b2a5-5b17a1c0444c)
Untuk semua keperluan pertanyaan bisa dilihat dibawah ini :
![image](https://github.com/user-attachments/assets/d36739c4-02a7-45f9-a3fe-12e7eb69abba)

saya bisa memperlihatkan prompt dari chatgpt untuk untuk pesan apa yang ditinggalkan oleh sang attacker 
![image](https://github.com/user-attachments/assets/811ad49a-c817-499a-adde-515fbc405ff2)
Saya seharusnya bisa mendemokannya

## Illegal Breakthrough
![image](https://github.com/user-attachments/assets/fcfe0f39-a205-4d52-9068-1d734f37c62c)
![image](https://github.com/user-attachments/assets/a50f8b81-51e0-4ece-b1cf-5d9e200cf23d)
Ya! seperti itu terminal saya, banyak bruteforce karena masaalah formatting 
![image](https://github.com/user-attachments/assets/9acd3ba3-c712-4893-808a-4a6ff6c12dc0)
Diaatas adalah segala info untuk mengerjakan soal ini (endpoint, user:ppwd, tools)
Untuk IP dan port?
![image](https://github.com/user-attachments/assets/044c26f4-7327-4425-b5d1-a6bce5a4422e)

## Packet Barrage
![image](https://github.com/user-attachments/assets/e29f2542-bf16-4377-b899-dbda84a47fb0)
Karena keterbatasaan deadline 1 jam saya kirim attachment acak
isi file malware dan nama file?
![image](https://github.com/user-attachments/assets/88bd9bfd-cca6-49f3-a7b1-47b37e2beb31)
IP addrs?
![image](https://github.com/user-attachments/assets/08635d8d-6281-462d-92c7-478256479776)
total bruteforce adaalah angka stream tersebut -1 sehingga 1918-1 = 1917
Kodingan?
![image](https://github.com/user-attachments/assets/b516c05a-0237-493f-b8f7-3ebdd2ceca6c)











