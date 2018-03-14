# Aplikasi Web "PageKit"
<h1 align="center"><img src="https://pagekit.com/storage/pagekit-logo.svg" width="500px"></h1>

[Sekilas Tentang](#sekilas-tentang) | [Instalasi](#instalasi) | [Konfigurasi](#konfigurasi) | [Otomatisasi](#otomatisasi) | [Maintenance](#maintenance) | [Cara Pemakaian](#cara-pemakaian) | [Pembahasan](#pembahasan) | [Referensi](#referensi)
:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:

## Sekilas Tentang 
[`^ kembali ke atas ^`](#aplikasi-web-pagekit)

PageKit merupakan aplikasi *web content management system*. PageKit digunakan untuk mempermudah pengguna dalam membangun situs web. Pagekit adalah CMS modular dan ringan yang dibangun dengan teknologi modern. Dengan market share kurang dari 0.1% dan 1,465 *website* yang aktif menggunakan CMS ini, menjadikan Pagekit sebagai salah satu CMS untuk *blogging* terpopuler di dunia, tepatnya berada di posisi ke-9 setelah Posthaven. PageKit memiliki beberapa fitur, di antaranya, menyediakan pengaturan untuk membuat halaman baru (contoh: membuat halaman untuk *blog*, mengorganisasi *file*, dan personalisasi *web*).

## Instalasi
[`^ kembali ke atas ^`](#aplikasi-web-pagekit)

#### Kebutuhan
- Apache 2.2+ atau Nginx
```
$ sudo apt install apache2
```

- MySQL Server 5.1+ atau SQLite 3
```
$ sudo apt install mysql-server
```

- PHP versi 5.5.9+
```
$ sudo apt install php
```

- Ekstensi PHP yang harus aktif: JSON, Session, ctype, Tokenizer, SimpleXML, DOM, mbstring, PCRE 8.0+, ZIP dan PDO dengan *driver* MySQL atau SQLite
```
$ sudo apt install libapache2-mod-php
$ sudo apt install php-mysql
$ sudo apt install php-gd php-mcrypt php-mbstring php-xml php-ssh2
$ sudo service apache2 restartapt-get install zip unzip
```

- (*opsional*) Ekstensi PHP: curl, iconv, XML Parser, APC atau XCache untuk *caching*
```
$ sudo apt-get install phpmyadmin php-mbstring php-gettext
```

#### Cara instalasi
1. Unduh arsip ZIP instalasi Pagekit dan simpan ke dalam direktori pagekit. 
```
$ mkdir pagekit
$ cd pagekit
$ wget bit.ly/komdatPagekit
```

2. *Unzip* arsip yang sudah terunduh. 
```
$ unzip pagekit-1.0.11.zip
```

3. Pindahkan direktori pagekit ke /var/www/html/ (direktori sekarang "pagekit")
```
$ sudo mv ../pagekit/ /var/www/html/
```

4. Selanjutnya buka http://localhost (localhost -> alamat IP atau URL kamu). Selanjutnya ikuti langkah-langkah untuk konfigurasi.
	- Pengaturan Bahasa
	- Konfigurasi Database
	- Pengaturan Informasi Situs
	- Selesai! (Tampilan halaman *admin*)
	
## Maintenance
[`^ kembali ke atas ^`](#aplikasi-web-pagekit)

PageKit menyediakan fitur *maintenance* apabila admin web ingin melakukan perbaikan pada situs. 
1. Pada halaman *dashboard* admin (http://URL/admin/dashboard), klik tombol *hamburger* di pojok kiri atas, kemudian pilih ikon *Site*
2. Pada halaman *site*, pilih tab *Settings*, kemudian pilih submenu *Maintenance*
3. Setelah itu, centang *Put the site offline and show the offline message.*, kemudian isikan pesan yang akan ditampilkan untuk memberitahukan bahwa situs sedang ada perbaikan (opsional), lalu tambahkan gambar (opsional).
4. Terakhir, tekan tombol *Save* kemudian coba akses kembali situsnya (dalam keadaan tidak *login* sebagai admin).

## Cara Pemakaian
[`^ kembali ke atas ^`](#aplikasi-web-pagekit)

1. Tampilan aplikasi web
	1. Tampilan utama (*default*)
	2. Tampilan halaman blog (*default*)
	3. *Dashboard admin*
	
2. Fungsi-fungsi utama
	1. Register *User* Baru
		* Fungsi ini digunakan apabila ada *guest* yang ingin menjadi penulis blog atau agar dapat menulis komentar di blog. Langkah pertama, lihat *widgets Login* yang terletak di *sidebar* kanan. Kemudian, klik tombol *Sign Up*
		
		* Setelah itu, isikan semua *field* yang diberikan
	
		* Setalahnya, klik tombol *Sign Up* dan akan muncul pemberitahuan bahwa *user* telah berhasil didaftarkan.
	
		* Lakukan login, kemudian akses http://YourURL/admin/.
	
	2. Buat Pos
		* Untuk membuat *post*, di halaman *dashboard admin*, klik *hamburger button* yang terletak di pojok kiri atas, kemudian pilih *Blog*
	
		* Setelah itu, klik tombol *Add Post*

		* Isikan *post* yang ingin dibuat, setelah selesai klik tombol *Save*
	
	3. Buat *Page* Baru
		* Untuk membuat *page*, dari halaman *dashboard admin*, klik *hamburger button* yang terletak di pojok kiri atas, kemudian pilih *Site*

		* Setelah itu, klik tombol *Add Page*, kemudian pilih *Page*

		* Isikan *page* yang ingin dibuat sesuai *field* yang tersedia, kemudian klik tombol *Save*

	4. Mengganti Tema
		* Unduh koleksi tema di halaman *Marketplace* dan pilih tab Tema

		* Pilih salah satu tema, kemudian klik

		* Setelah terunduh, klik tombol *Enable* untuk mengaktifkan tema

		* Tema yang telah terunduh dapat dilihat di halaman *System* dan pilih tab *Theme*
	
	5. Menambahkan Widget
		* Buka halaman *Site* melalui menu di *hamburger button*, kemudian pilih tab *Widgets*
	
		* Klik tombol *Add Widgets*

		* Pilih salah satu kategorinya, *Menu* untuk menambahkan *list* halaman, *Text* untuk menambahkan ukiran kata-kata, dan *Link* untuk menambahkan pranala ke halaman lain.

		* Isikan *field* yang perlu isi, kemudian atur tata letaknya di menu *dropdown* sebelah kanan

		* Setelah selesai, klik *Save*. Cek halaman awal apakah *widget* sudah berhasil ditambahkan.

	6. Manajemen *User* dan Mengatur *Permission* berdasarkan *role*
		* Buka halaman *Users* melalui menu di *hamburger button*
	
		* Diberikan *list* *user* yang sudah terdaftar, apabila *role*-nya adalah *admin*, maka ia bisa menghapus/memblokir *user*

		* Untuk mengatur *Permission* untuk *Role* tiap-tiap *user*, klik tab *Permission*.
		* Di situ, kita bisa memberikan/melepas izin untuk tiap jenis aktivitas yang dapat dilakukan.


## Pembahasan
[`^ kembali ke atas ^`](#aplikasi-web-pagekit)

Aplikasi web PageKit merupakan CMS yang bisa dikatakan baru, namun memiliki beberapa fitur yang diunggulkan, di antaranya:
1. Dibangun menggunakan *framework* PHP Symfony dan Vue.js
2. Tampilan yang modern dan *responsive*, namun tetap terlihat sederhana
3. Proses instalasi dan konfigurasi yang sangat mudah dan serba otomatis
4. Terdapat editor teks berupa Markdown dan HTML
5. Terdapat *file manager* untuk mengatur *file* apa saja yang diunggah ke server
6. Personalisasi dan pengaturan halaman situs yang tidak rumit
7. Pengaturan kontrol *cache*

Namun, dari keunggulan yang diberikan, masih terdapat beberapa kekurangan, di antaranya:
1. Variasi tema dan ekstensi (*plugin*) yang diberikan masih terbilang sedikit, selain itu hanya bisa menggunakan tema yang disediakan, tidak dapat dikustomisasi atau dibuat sendiri.
2. Walaupun terbilang mudah, tidak seperti wordpress yang memiliki *live preview*, untuk mengatur tata letak *widget* yang akan ditampilkan di situs masih menggunakan menu *dropdown*.

### Perbandingan dengan aplikasi web 'Subrion'
Sama halnya dengan PageKit, Subrion merupakan CMS yang digunakan untuk mempermudah pengguna membangun situs web. Dengan berbagai macam fitur yang ditawarkan, terdapat beberapa kesamaan, di antaranya:
1. Subrion dapat digunakan untuk membuat situs blog
2. Memiliki *user management* lengkap dengan *permission* sesuai *role*-nya
3. Kustomisasi halaman (membuat baru, menghapus, mengubah status (aktif/inaktif/draft))
4. Terdapat *storage management* untuk mengatur *file-file* yang terunggah ke server

Namun ada beberapa hal yang perlu diperhatikan sebagai ciri pembeda.
1. Halaman *admin* PageKit memiliki tampilan sederhana (tidak banyak *content* yang ditampilkan dalam suatu halaman, sedangkan Subrion terkesan menampilkan banyak *content*
2. Terdapat fitur unik di Subrion, yaitu adanya fitur *SQL Tools*, tanpa perlu membuka *phpMyAdmin* kita dapat melihat isi *database*-nya
3. Subrion juga dilengkapi dengan fitur keamanan di antaranya HTTPS, anti-CSRF, Build-in Captcha), sedangkan PageKit hanya pengaturan HTTPS saja yang ada

## Referensi
[`^ kembali ke atas ^`](#aplikasi-web-pagekit)

1. [About | PageKit](https://pagekit.com/about) - PageKit
2. [How To Rewrite URLs with mod_rewrite for Apache on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-rewrite-urls-with-mod_rewrite-for-apache-on-ubuntu-16-04) - DigitalOcean
3. [Installation | PageKit](https://pagekit.com/docs/getting-started/installation) - PageKit
3. [CLI | Pagekit](https://pagekit.com/docs/developer/cli) - PageKit