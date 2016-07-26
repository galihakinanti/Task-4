#Log Selasa, 26 Juli 2016

### Aktivitas yang dikerjakan
	1. Cara menginstall nodeBB menggunakan windows

    
### Source yang digunakan
* https://docs.nodebb.org/en/latest/installing/os/windows8.html
* https://media.readthedocs.org/pdf/nodebb-francais/latest/nodebb-francais.pdf

Beberapa software yang diperlukan sebelum menginstall nodeBB.

Pertama, instal program-program berikut terlebih dahulu:
* https://windows.github.com/
* https://nodejs.org/dist/v0.10.35/
* http://imagemagick.org/script/binary-releases.php#windows/
* https://www.python.org/ftp/python/2.7.8/python-2.7.8.msi
* https://github.com/MSOpenTech/redis/releases
* https://www.microsoft.com/en-us/download/details.aspx?id=44914



### Running nodeBB
Start Redis Server

Catatan : Lokasi Redis Server :
###### C:\Program Files\Redis\StartRedisServer.cmd


Buka Git Shell, dan ketik perintah berikut. Clone NodeBB repo:

	git clone -b v1.x.x https://github.com/NodeBB/NodeBB.git

Enter directory :

	cd NodeBB
Install dependencies:

	npm install
Run interactive installation:

	node app.js
You may leave all of the options as default.

Proses telah selesai! Setelah instalasi, maka jalankan:

	node app.js
