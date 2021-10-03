#Tugas 1 instruksi penggunaan git dan gitHub


## *Installasi git pada OS Linux Ubuntu*
Pada tahap ini menggunakan **APT**

1. Mulai dengan mengupdate indeks paket
```bash
sudo apt-get update
```

2. Jalankan perintah installasi
```bash
sudo apt-get install git
```

3. untuk verifikasi coba cek dengan ketik perintah berikut pada terminal
```bash
git --version
```


## *Konfigurasi Git*
untuk mengatur informasi pengguna maka git harus dikonfigurasi dahulu

```bash
git config --global user.name "mogarnurhandhi"
git config --global user.email "mogarnurhandhi@gmail.com"
```
dan untuk melihat dan verifikasi perubahan ketikan perintah 

```bash
git config --list
```


## *Pengelolaan repo sendiri*
sebelum memulai operasi ini ada baiknya membuat **personal acces token** adapun caranya tertulis di (https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)



## *Pembuatan repository*
adapun caranya sebagai berikut
1. pada pojok kanan atas ada navigasi akun dan tanda **+** klik tanda tersebut serta pilih **New Repository**
2. setelah itu akan muncul isian identitas untuk repo, isi saja bagian nama repo kita, pada bagian ini juga bisa mengatur repo untuk public atau privat 
3. memang ada isian isian lain yang bersifat opsional sesuai kebutuhan
4. klik `Create Repository`



## *Clone repository*
clone adalah proses menduplikasi file repo yang ada di gitHub ke komputer local 
adapun caranya sebagai berikut, bisa menggunakan **SSH** atau **HTTPS** dan kali ini menggunakan cara kedua

```bash
(base) mo21y@mo21y-HP-Notebook:~$ git clone https://github.com/mogarnurhandhi/01-git-github.git
Cloning into '01-git-github'...
warning: You appear to have cloned an empty repository.
```

akan muncul peringatan seperti diatas karena repo tersebut kosong
dan untuk mengelola repo tersebut harus berpindah directory sesuai lokasi repo tersebut seperti berikut

```bash
(base) mo21y@mo21y-HP-Notebook:~$ cd 01-git-github/
(base) mo21y@mo21y-HP-Notebook:~/01-git-github$
```


## *Branching and Merging*
fitur ini digunakan untuk menambahkan atau mengubah isi dari **main** tapi meminimalisir terjadinya bentrok atau konflik karena membuat cabang dari **main** itu sendiri

untuk melihat cabang yang sudah ada dengan perintah
```bash
git branch
```
jika belum ada hanya akan muncul master/main saja

Dan untuk membuat cabang baru perintahnya adalah
```bash
(base) mo21y@mo21y-HP-Notebook:~$ git brach edit_baru
```

setelah itu pindah kecabang yang baru dengan perintah
```bash
(base) mo21y@mo21y-HP-Notebook:~$ git checkout edit_baru
```

kita bisa menambahkan file kedalamnya atau sekedar argumen
```bash
(base) mo21y@mo21y-HP-Notebook:~$ git add -A
(base) mo21y@mo21y-HP-Notebook:~$ git commit -m "isi dari readme"
```

untuk menggabungkan **cabang** dan **main** kita dapat menggunakan Merging, ketikan perintah ini diterminal
```bash
(base) mo21y@mo21y-HP-Notebook:~$ git checkout master
```
untuk berpindah ke main/master dahulu
berikutnya untuk penggabungan perintahnya
```bash
(base) mo21y@mo21y-HP-Notebook:~$ git merge edit_baru
```


## *Sinkronasi*
mungkin ada kondisi dimana kita mengedit repo lokal tidak menggunakan komputer utama dan kita berpindah lagi dengan komputer lain
untuk itu perlu dilakukan sinkronasi dengan perintah 

```bash
(base) mo21y@mo21y-HP-Notebook:~$ git pull
```
