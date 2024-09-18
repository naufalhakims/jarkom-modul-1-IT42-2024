# jarkom-modul-1-IT42-2024

# Langsung saja ini adalah write-up nya
# Naufal Syafi' Hakim
# 5027231022
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











