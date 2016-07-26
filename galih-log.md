#Log Senin, 25 Juli 2016

### Aktivitas yang dikerjakan
	1. Mencari tau nodeBB itu seperti apa dan bagaimana.
    
### Source yang digunakan
https://community.nodebb.org/
    
Didalam nodeBB terdapat recent topics dan categories, yang dimana topiknya itu selalu berbeda-beda atau bisa disebut juga topik terbaru. Sedangkan categoris yaitu beberapa kategori atau fitur-fitur yang terdapat didalam nodeBB.

### Recent Topics
Dalam nodeBB yang saya baca ini memiliki recent topics, diantaranya:
#### 1.Nodebb-theme-material v2.0 published.

Nodebb-theme-material v2.0 sekarang dipublikasikan ke npm.
Kita dapat menginstall-nya dari ACP "Plugins".

Cara menginstalasi tema untuk NodeBB menggunakan Google Material Design:
-- Instal tema ini menggunakan "Plugins" di halaman NodeBB ACP
-- Setelah menginstalas lalu beralih dengan menggunakan tema "Themes" di halaman ACP
-- Restart NodeBB

#### 2.Error in a plugin blocks another plugin.

Misalkan untuk memiliki dua plugin yang terpisah.
Plugin pertama:
"hook": "action:user.updateProfile", "method": "usernameUpdate"
Di library dan dalam method "usernameUpdate" saya kira perlu menambahkan:
return next(new Error("Username already exist"));	//It is an example it could be another exception
Plugin kedua:
Saya ingin menghapus akun ketika pengguna mengklik tombol "hapus akun" jadi ketika saya klik tombol yang ada pada plugin pertama, maka lakukan operasi dibawah ini:
user.updateProfile(id_corrente, {
				'username': username_modificati,
				'slug': slug_modificati,
				'email': '',
				'password': username_modificati
			}, function(err, update_result) {
				if (err ) {
					return next(err);
				}

Metode ini gagal karena err dari plugin pertama ditangkap dari "if (err)". Plugin pertama bekerja dengan baik dan Plugin kedua tidak bekerja.

Source : https://community.nodebb.org/topic/9266/the-error-in-a-plugin-blocks-another-plugin

#### 3.[nodebb-plugin-ignore-users] Ignore Users for NodeBB

Beberapa informasi tentang cara mengabaikan posting dari pengguna tertentu, diantaraya :
* Anda dapat mengabaikan posting pengguna saat membaca threads. Di sebelah kanan setiap nama pengguna akan muncul ikon mata, menekan ikon yang akan mengabaikan atau jangan abaikan pengguna itu.
* Anda juga dapat mengabaikan pengguna dari profil pengguna. Opsi ini terletak di dropdown profil pengguna.
* Dari halaman profil Anda, Anda dapat melihat daftar pengguna yang Anda abaikan dan Anda memiliki pilihan untuk jangan abaikan mereka juga.
* Jika Anda memiliki pengguna yang diabaikan, Anda tidak dapat melihat postingan-nya, Anda akan melihat teks umum saja dan sistem akan memberitahu Anda bahwa pengguna diabaikan dan posting akan muncul sendiri.

Source : https://community.nodebb.org/topic/4543/nodebb-plugin-ignore-users-ignore-users-for-nodebb

### Beberapa kategori yang ada didalam nodeBB
1. Announcements
2. General Discussion
3. NodeBB Development
4. NodeBB Plugins
5. NodeBB Themes
6. Testing Ground
7. Technical Support
8. Tutorials

Beberapa kategori diatas, kita bisa memposting apapun yang sesuai dengan masing-masing kategori tersebut. Dan user lain pun dapat memberi komentar terhadap postingan yang kita buat.
