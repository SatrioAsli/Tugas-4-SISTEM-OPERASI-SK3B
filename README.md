# Tugas-4-SISTEM-OPERASI-SK3B
Nama    :Satrio Joronggur Mahendra
Kelas   : SK3B
NIM     :09011282328092

1. Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan standard output ke file
baru.

![Screenshot 2024-09-13 191456](https://github.com/user-attachments/assets/52f48260-a287-4f1f-83c7-d0d0fbd84067)
![Screenshot 2024-09-13 191536](https://github.com/user-attachments/assets/b9949e51-7968-4438-aa8b-044c6d05a397)


kita gunakan command ls -al untuk menampilkan secara lengkap direktori yang aktif kemudian kita gunakan command seperti ini : ls - al > daftar_direktori.txt agar output dari ls -al bisa dimasukkan ke dalam file bernama daftar_direktori.txt dan untuk mengecek apakah output dari ls -al tersimpan kedaftar_direktori.txt kita cukup gunakan command cat daftar_direktori.txt


2. Lihat daftar secara lengkap pada direktori /etc/paswd, belokkan tampilan standard outputke file baru tanpa menghapus file baru sebelumnya. \

   ![Screenshot 2024-09-13 192831](https://github.com/user-attachments/assets/be6d5047-62df-4125-91ee-479974815b7c)
![Screenshot 2024-09-13 192815](https://github.com/user-attachments/assets/6ca906a6-f7d0-43e4-be74-a1220f902f50)


 kita gunakan command cat /etc/passwd Dikarenakan passwd bukanlah sebuah direktori, kemudian enter untuk melihat isinya, bisa juga langsung simpan output nya ke daftar_direktori.txt dengan menambahkan >> daftar_direktori.txt setelah command cat (note : dikarenakan kita ingin menyimpan output passwd ke daftar_direktori.txt tanpa menghapus isi file lama, maka kita harus menggunakan ">>" jangan ">" karena jika ">" maka isi file lama akan diganti dengan isi file yang baru)


3. Urutkan file baru dengan cara membelokkan standard input.
![Screenshot 2024-09-13 193302](https://github.com/user-attachments/assets/89196b84-3469-4708-b37c-ea293809329c)

Setelah kita berhasil menyimpan output passwd ke filebaru.txt langkah selanjutnya adalah mengurutkan isi file nya sesuai abjad dengan membelokkan standar input, jika sebelumnya kita membelokkan standar output menggunakan >> sekarang kita gunakan << untuk membelokkan standar input, jadi command nya adalah sort < daftar_direktori.txt lalu enter maka isi file dari daftar_direktori.txt akan terurutkan.

4. Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut. 
![Screenshot 2024-09-13 193538](https://github.com/user-attachments/assets/2f4ba420-5e69-4999-8f1a-5cfed4538971)


Di bagian ini, hasil dari pengurutan isi filebaru.txt berhasil dilakukan, kita lakukan penyimpanan dari output nya itu ke file yang bernama daftar_baru.txt menggunakan command sort < daftar_direktori.txt > daftar_baru.txt

5. Buatlah direktori latihan6 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt. 
![Screenshot 2024-09-13 194555](https://github.com/user-attachments/assets/63353525-8268-4cc0-a8ac-25c1caeb8e47)

Pertama-tama kita buat direktori bernama latihan6 dan berhasil, lalu kita buat lagi direktori dengan nama yang sama dan sudah pasti tidak berhasil karena nama yang digunakan itu sama, output dari error itu kita masukkan ke file yang bernama rmdirerror.txt dengan cara mkdir latihan6 2> rmdirerror.txt, "2>" itu adalah command untuk membelokkan standar output error ke sebuah file)

6. Urutkan kalimat berikut :

Jakarta

Bandung

Surabaya

Padang

Palembang

Lampung

Dengan menggunakan notasi here document (<@@@ …@@@)
![Screenshot 2024-09-13 195002](https://github.com/user-attachments/assets/baf63d03-a7b9-47b1-b653-ee676e97df01)

Untuk mengurutkan suatu inputan secara langsung, kita gunakan command sort <<@@@ kemudian enter dan ketik nama kota seperti Jakarta, Bandung dll setelah sudah selesai ketik @@@ maka inputan data yang kita ketik tadi akan terurut dan otomatis ditampilkan (command "<<@@@" ini adalah notasi yang berfungsi untuk menyelesaikan/menghentikan input ketika kita sudah selesai menginput data yang ingin diurutkan)

7. Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru.
![Screenshot 2024-09-13 200010](https://github.com/user-attachments/assets/acbfc5c2-2a67-49a6-87a6-a29954c85696)
kita cukup gunakan command wc "nama file yang ingin dihitung jumlah barisnya" contohnya wc  lalu enter maka akan muncul output "74 343 5451 fDdaftar_baru.txt" angka angka itu mewakilkan jumlah baris, kata dan karakter (74 = jumlah baris, 343 = jumlah kata, 5451 = jumlah karakter)


8. Gunakan perintah di bawah ini dan perhatikan hasilnya.
9. 
$ cat /etc/passwd | sort | pr –n | grep tty03

$ find /etc –print | head

$ head /etc/passwd | tail –5 | sort


![Screenshot 2024-09-13 200743](https://github.com/user-attachments/assets/cbac122f-6e16-4e36-84d6-8e7a83ad28c9)


A. cat /etc/passwd | sort | pr -n | grep tty03
Penjelasan : pada baris kode ini berfungsi untuk mencari entri dalam file /etc/passwd yang berisi informasi terkait dengan "tty03", setelah isi file tersebut diurutkan dan diberi nomor baris. Namun, dikarenakan tidak ada entry di tty03 di dalam /etc/passwd maka tidak ada output yang muncul (cat /etc/passwd untuk menampilkan isi passwd, sort untuk mengurutkan nya, pr -n untuk memberi nomor pada setiap baris)

B. find /etc –print | head
Penjelasan : pada baris kode ini berfungsi untuk mencari semua file dan direktori pada /etc kemudian di tampilkan, tapi karena saya menggunakan command head maka yang tampil hanya 10 baris pertama saja

C. head /etc/passwd | tail –5 | sort
Penjelasan : pada baris kode ini berfungsi untuk menampilkan 10 baris pertama dari isi passwd kemudian diambil 5 baris terakhir lalu di urutkan kemudian ditampilkan sebagai output


9. Gunakan perintah $ who | cat | cat | sort | pr | head | cat | tail dan perhatikan hasilnya.
    ![Screenshot 2024-09-13 201158](https://github.com/user-attachments/assets/223c948b-3496-4b26-96f0-de12c926ccb8)
Command ini berfungsi untuk mengurutkan daftar pengguna yang sedang login, lalu memformat tampilannya menjadi beberapa kolom dengan header halaman. Setelah itu, perintah hanya menampilkan 10 baris pertama, dan hasil akhirnya tidak berubah karena penggunaan cat | tail hanya meneruskan output dari head tanpa ada perubahan apa pun.
