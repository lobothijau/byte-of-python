# Pemasangan Python {#installation}

Saat menemukan kata "Python 3" di buku ini, yang dimaksud adalah semua versi Python yang lebih atau sama dengan versi [Python {{ book.pythonVersion }}](https://www.python.org/downloads/).

## Pemasangan Python di Windows

Kunjungi https://www.python.org/downloads/ dan unduh versi terakhirnya. Saat tulisan dibuat, versi terakhirny adalah Python 3.5.1.
Cara pemasangannya sama seperti aplikasi Windows lain.

Perlu diketahui apabila menggunakan Windows sebelum Vista, maka pembaca hanya bisa memasang [Python 3.4](https://www.python.org/downloads/windows/) karena versi setelahnya meminta versi Windows yang baru.

CAUTION: Pastikan pembaca memberi centang opsi `Add Python 3.5 to PATH`.

Untuk mengganti lokasi pemasangan, klik `Customize installation`, lalu `Next` dan masukkan `C:\python35` (atau lokasi lain yang diinginkan) sebagai lokasi pemasangan.

Jika tidak memberi centang opsi `Add Python 3.5 PATH` sebelumnya, beri centang `Add Python to environment variables`. Opsi ini memberikan hasil yang sama dengan `Add Python 3.5 to PATH` di layar pertama pemasangan.

Kita bisa memilih untuk memasang Launcher untuk semua pengguna atau tidak, dan opsi ini tidak begitu berpengaruh. Launcher dipakai untuk menukar versi-versi Python yang terpasang. 

Jika path belum diatur dengan benar (dengan memberi cek `Add Python 3.5 Path` atau `Add Python to environment variables`), maka ikuti langkah di bagian berikut (`DOS Prompt`) untuk memperbaikinya. Jika sudah, langsung ke bagian `Running Python prompt on Windows`.

NOTE: Untuk mereka yang sudah mengenal pemrograman, jika sudah familiar dengan Docker, periksa [Python in Docker](https://hub.docker.com/_/python/) dan [Docker on Windows](https://docs.docker.com/windows/).

### DOS Prompt {#dos-prompt}

Jika ingin bisa memakai Python dari _command line_ Windows atau nama lainnya DOS prompt, maka kita perlu mengatur variabel PATH. 

Untuk Windows 2000, XP, dan 2003, klik `Control Panel` -> `System` -> `Advanced` -> `Environment Variables`. Klik variabel bernama `PATH` dibagian _System Variables_, lalu pilih `Edit` dan tambahkan `;C:\Python35` (pastikan bahwa folder ini ada, mungkin nama foldernya bisa berbeda tergantung versi yang diunduh) di akhir isi yang sudah ada. Sekali lagi, gunakan nama folder yang ada.

<!-- The directory should match pythonVersion variable in book.json -->
Untuk versi yang lebih lama, buka file `C:\AUTOEXEC.BAT` dan tambahkan baris `PATH=%PATH%;C:\Python35` lalu restart sistem. Untuk Windows NT, gunakan file `AUTOEXEC.NT`.

Untuk Windows Vista:

- Klik Start dan pilih `Control Panel`
- Klik System, dibagian sebelah kanan pembaca akan melihat "View basic information about your computer"
- Di sebelah kiri ada pilihan yang salah satunya adalah `Advanced system settings`. Klik menu tersebut.
- Tab `Advanced` di dialog box `System Properties` terlihat. Klik button `Environment Variables` dibagian kanan bawah.
- Dikotak bagian bawah berjudul `System Variables`, scroll ke bawah ke bagian path dan klik tombol `Edit`. 
- Ubah path-nya dengan data yang diperlukan. 
- Restart sistem. Vista tidak akan membaca perubahan path sebelum restart dilakukan.

Untuk Windows 7 dan 8:

- Klik kanan ikon Computer yang ada di desktop dan pilih `Properties` atau klik `Start` dan pilih `Control Panel` -> `System and Security` -> `System`. Klik `Advanced system settings` di sebelah kiri lalu pilih tab `Advanced`. Di bawahnya klik `Environment Variables` dan di bawah `System variables`, cari variabel `PATH`, pilih lalu tekan `Edit`.
- Dibagian akhir baris tersebut, tambahkan `;C:\Python35` (pastikan bahwa folder ini ada, mungkin nama foldernya bisa berbeda tergantung versi yang diunduh). Sekali lagi, gunakan nama folder yang sesuai.
- Jika isinya adalah `%SystemRoot%\system32;` baris tadi akan menjadi `%SystemRoot%\system32;C:\Python36` <!-- The directory should match pythonVersion variable in book.json -->
- Klik `OK` dan selsai. Tidak perlu melakukan restart dan kita perlu menutup dan membuka lagi aplikasi _command line_.

Untuk Windows 10:

Windows Start Menu > `Settings` > `About` > `System Info` (tiap menu akan membuka ke sebelah kanan) > `Advanced System Settings` > `Environment Variables` (ada di bagian bawah) > (pilih variabel `Path` dan klik `Edit`) > `New` > (tuliskan folder lokasi python. Misalnya, `C:\Python35\`)


### Menjalankan prompt Python di Windows

Untuk user Windows, kita bisa menjalankan interpreter Python di _comand line_ jika kita sudah [mengatur varibel `PATH` dengan benar](#dos-prompt).

Untuk membuka terminal di Windows, klik tombol start dan klik `Run`. Pada dialog box yang muncul, ketikkan `cmd` dan tekan tombol `[enter]`. 

Lalu, ketik `python` dan pastikan tidak ada error. 

## Pemasangan di Mac OS X

Untuk user Mac OS X, gunakan [Homebrew](http://brew.sh): `brew install python3`.

Untuk memastikan pemasangan berhasil, buka terminal dengan kombinasi tombol `[Command + Space]` (untuk membuka kotak pencarian Spotlight), tuliskan `Terminal` dan tekan tombol `[enter]`. Sekarang, jalankan `python3` dan pastikan tidak ada error.

## Pemasangan di GNU/Linux

Untuk user GNU/Linux, gunakan _package manager_ masing-masing distro untuk memasang Python 3, misalnya di Debian dan Ubuntu:`sudo apt-get update && sudo apt-get install python3`.


Untuk memastikan pemasangan berhasil, buka terminal lewat aplikasi `Terminal` atau menekan tombol tombol `Alt + F2` dan menulis `gnome-terminal`. Jika tidak dapat bekerja, silahkan lihat dokumentasi sistem distro GNU/Linuix masing-masing. Jalankan perintah `python3` dan pastikan tidak ada error.

Kita bisa melihat versi Python dengan menjalankan perintah:

<!-- The output should match pythonVersion variable in book.json -->
```
$ python3 -V
Python 3.6.0
```

NOTE: `$` adalah bagian _prompt_ shell. Ia mungkin berbeda tergantung pengaturan masing-masing sitem operasi sehingga disini penulis hanya akan mengindikasikannya melalui simbol `$`.

CAUTION: Pesan keluarannya mungkin terlihat berbeda di komputer pembaca, tergantung program Python yang terpasang.

## Kesimpulan

Mulai dari sini, kita akan mengasumsikan bahwa Python sudah terpasang di sistem. 

Selanjutnya, kita akan menulis program Python kita yang pertama. 
