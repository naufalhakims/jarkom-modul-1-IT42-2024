# jarkom-modul-1-IT42-2024

### Langsung saja ini adalah write-up nya

#### Rizzset 
Begini kira-kira saya mendapatkan flag
![image](https://github.com/user-attachments/assets/15543682-b57f-4941-9dcb-453774d53ae3)
Oke jadi pertama kita lihat gambar dibawah ini :
![image](https://github.com/user-attachments/assets/82d3ce01-7674-49b7-bd9b-92c64cc3e289)

Dapat terlihat bahwa domain www.its.ac.id dan IP nya terpampang jelas sehingga 2 pertanyaan awal sudah solve (domain dan IP)
Selanjutnya untuk pertanyaan JARM Fingerprint saya mengclone github JARM sendiri lalu masukkan ke folder local saya dan saya mengetikan python jarm.py untuk mendapatkan string yang diinginkan. Kira-kira begini :
![image](https://github.com/user-attachments/assets/6ca3fc2f-d7f8-4fd8-923f-f916d695c82d)
Setelah itu sudah mendapatkan flagnya.

#### EZ
Pertama membuka wireshark saya langsung follow salah satu baris dan mencari-cari clue dan menemukan ini :
![Screenshot 2024-09-19 001621](https://github.com/user-attachments/assets/22544583-fc88-4d3a-8d4b-17f086fa91f5)
clue nya adalah string "jawabannya jawaban". Lalu selanjutnya terdapat clue Destination Port pada paket seperti ini 
![image](https://github.com/user-attachments/assets/6b718f90-d9c5-4c3f-b54f-d042ebbd59d0)
Maka dari ini saya mendapatkan flagnya, kira-kira beginilah terminalnya 
![image](https://github.com/user-attachments/assets/d528b2d7-1c59-4c3d-802f-547dc9b94a07)

#### FTPLOGIN
Pada ftplogin begini terminal saya :
![Screenshot 2024-09-19 002340](https://github.com/user-attachments/assets/52b32f3f-e61c-4e74-938b-b276c6f7fe66)
Caranya adalah dengan bruteforce mencari follow stream yang memiliki login successfull
![image](https://github.com/user-attachments/assets/5e3bca6b-2486-4f5b-b2d7-a04902d43f97)

#### Advance Sanity Check
Begini terminal saya
![image](https://github.com/user-attachments/assets/e04cc264-4898-4784-8578-324e955bf0e9)
Username?
![image](https://github.com/user-attachments/assets/2b6ceded-e16a-467c-93b2-9d9864bcb0cf)
Filename?
![Screenshot 2024-09-19 003336](https://github.com/user-attachments/assets/7df020ca-9315-40c2-a4a4-a36a05137ce8)
Bagaimana saya menemukannya ya follow stream lait-liat aja yang lain.

Cara mendecodenya saya seperti ini
![image](https://github.com/user-attachments/assets/b2aee3ea-fca7-4c88-8e61-2ac3f29d44f8)






