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
