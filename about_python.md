# Tentang Python

Python adalah salah satu bahasa langka yang diklaim _sederhana_ dan _powerful_ di saat yang bersamaan. Pembaca akan melihat bagaimana asiknya saat memprogram solusi permasalahan daripada mengurus sintaks dan struktur bahasa yang dipakai untuk memprogram. 

Perkenalan resmi untuk baahsa Python adalah:

> Python merupakan bahasa pemrograman yang _powerful_ dan mudah dipelajari. Bahasa ini memiliki struktutr data tingkat-tinggi yang efisien dan sederhana namun efektif dengan pendekatan pemrograman berorientasi objek. Sintaks Python yang elegan dan dinamis, bersama dengan sifat _interpreted_-nya, membuat Python menjadi bahasa yang ideal untuk skripting dan _rapid application development_ dibanyak area dan hampir disemua sistem.

Penulis akan membahas sebagain besar fitur ini secara lebih detail di bab berikutnya.

## Sejarah dibelakang namanya

Guido van Rossum, the creator of the Python language, named the language after the BBC show "Monty
Python's Flying Circus". He doesn't particularly like snakes that kill animals for food by winding
their long bodies around them and crushing them.

## Fitur-fitur Python

### Sederhana

Python adalah bahasa yang sederhana dan minimalistis. membaca sebuah program Python yang baik seperti membaca dalam Bahasa Inggris, meskipun Bahasa Inggris yang sangat terbatas! Sifatnya yang seperti pseudo-code ini meruapkan salah satu kelebihan terbesarnya. Python memungkinkan kita untuk konsentrasi pada solusi program daripada mengurusi bahasa itu sendiri. 

### Mudah Dipelajari

Seperti yang akan pembaca lihat, sangat mudah untuk mulai menggunakna Python. Ia memiliki sintaks yang luar biasa sederhana, seperti yang sudah dibahas sebelumnya.

### Free dan Open Source

Python merupakan contoh sebuah _FLOSS_ (Free/Libré and Open Source Software). Dalam istilah sederhananya, kita dapat mendistribusikan salinan perangkat lunak ini, membaca source code-nya, buat perubahan, dan menggunakan salah satu isinya dalam program free yagn baru. FLOSS berbasiskan konsep dimana sebuah komunitas berbagi pengetahuan. Inilah salah satu yang membuat mengapa Python sangat bagus - Ia sudah dibuat dan secara kontinyu dikembangkan oleh komunitas yang hanya ingin melihat Python yang lebih baik. 

### Bahasa Tingkat Tinggi

Saat menuis program dengan Python, kita tidak akan pernah memperdulikan detail tingkat rendah seperti mengurus memori yang dipakai program, dll. 

### Portabel

Karena sifatnya yang open-source, Python sudah dibuat agar dapat berjalan di berbagai sistem. Semua program Python kita dapat berjalan di sistem manapun tanpa perlu mengubah kodenya jika kita dapat menghindari penggunaan fitur-fitur yang hanya ada di sistem tertentu.

Kita bisa menggunakan Python di GNU/Linux, Windows, FreeBSD, Macintosh, Solaris, OS/2, Amiga, AROS, AS/400, BeOS, OS/390, z/OS, Palm OS, QNX, VMS, Psion, Acorn RISC OS, VxWorks, PlayStation, Sharp Zaurus, Windows CE dan PocketPC!

Kita bahkan bisa menggunakan layanan [Kivy](http://kivy.org) untuk membuat game di PC, iPhone, iPad, dan Android.

### Interpreted

Bagian ini perlu sedikit penjelasan.

Sebuah prgoram yang ditulis dalam bahasa terkompilasi seperti C atau C\++ perlu diubah dari bahasa sumber seperti C atau C\++ menjadi bahasa yang dimengerti oleh komputer (kode biner yaitu 0 dan 1) menggunakna sebuah kompiler dengan berbagai opsi dan flags. Saat program dieksekusi, linker/loader menyalin program dari hardisk ke memori dan mulai menjalankannya.

Python, sebaliknya tidak memerlukan proses kompilasi. Kita cukup menjalankan program langsung dari kode sumber. Dibelakang layar, Python mengubah kode sumber menjadi bentuk yang langsung dapat dipanggil bernama _bytecodes_ lalu menerjemahkannya menjadi bahasa yang dimengerti oleh komputer lalu mengeksekusinya. Semua ini, membuat penggunaan Python menjadi lebih mudah karena kita tidak perlu repot-repot mengkompilasi program, memastikan pustaka sudah terhubung dan termuat, dll. Hal ini juga membaut program Python menjadi lebih portabel, karena kita cukup menyalin program Python kita ke sistem komputer lain dan dia akan langsung berjalan!

### Berorientasi Objek

Python mendukung pemrograman prosedural juga pemrograman berorientasi objek. Dalam bahasa prosedural, program dibuat dengan prosedur atau fungsi yang hanya bertindak sebagai bagian program yang dapat dipakai berkali-kali. Dalam bahasa berorientasi objek, program dibuat dengan objek yang mengombinasikan data dan fungsionalitasnya. Python memiliki cara yang sederhana tapi sangat manjur untuk melakukan OOP, terutama saat dibandingkan bahasa besar lain seperti C++ atau Java.

### Extensible

Jika kita perlu membuat salah satu bagian kode untuk berjalna dengan sangat cepat atau memiliki bagian algoritma yang tidak ingin diperlihatkan, kita bisa menulis bagian kode tersebtu dengan C atau C++ lalu memanggilnya dari program Python.

### Embeddable

Kita bisa menyisipkan program Python di dalam program C/C++ yang memberiakn kemampuan _scripting_ untuk pengguna aplikasi.

### Memiliki Pustaka yang Besar

Python Standard Library sangatlah besar. Ia bisa membantu kita menyiapkan berbagai solusi yang sudah dibuat oleh orang lain seputar regular expression, documentation generation, unit testing, threading, databases, web browsers, CGI, FTP, email, XML, XML-RPC, HTML, WAV files, cryptography, GUI (graphical user interfaces), dan bagian lain yang bergantung pada sistem. Ingat, bahwa semua ini akan selalu tersedia dimanapun Python terpasang. Inilah filosofi _Batteries Included_ (_sudah termasuk baterai_) yang disematkan di Python.

Selain _standard library_, ada banyak pustaka lain yang bisa kita temukan di [Python Package Index](http://pypi.python.org/pypi).

### Kesimpulan

Python tentu merupakan sebuah bahasa pemrograman yang menarik dan _powerful_. Ia memiliki kombinasi performa dan fitur yang membuat proses penulisan program di Python lebih mudah dan menyenangkan. 

## Python 3 versus 2

Pembaca bisa melewati bagian ini jika tidak tertarik akan perbedaan antara "Python versi 2" dan "Python versi 3". Tapi mohon untuk menyadari versi mana yang dipakai. Buku ini ditulis untuk Python versi 3.

Ingat bahwa saat sudah memahami bagaimana menggunakan salah satu versi dengan baik, kita bisa mempelajari perbedaan yang ada dan menggunakan versi lainnya. Bagian yang lebih sulit adalah belajar pemrograman dan memahami dasar-dasar bahasa Python itu sendiri. Itu lah tujuan ditulisnya buku ini, setelah kita bisa mencapai tujuan tersebut, pembaca dapat menggunakan Python 2 atau Python 3 sesuai situasi yang dihadapi.

Untuk pembahasan perbedaan yang lebih detail antara Python 2 dan Python 3, lihat:

- [The future of Python 2](http://lwn.net/Articles/547191/)
- [Porting Python 2 Code to Python 3](https://docs.python.org/3/howto/pyporting.html)
- [Writing code that runs under both Python2 and 3](https://wiki.python.org/moin/PortingToPy3k/BilingualQuickRef)
- [Supporting Python 3: An in-depth guide](http://python3porting.com)

## Apa yang Programmer Katakan 

Pembaca mungkint ertarik untuk mengetahui apa komentar hacker-hacker terkenal seperti ESR tentang Python:

- _Eric S. Raymond_ adalah penulis "The Cathedral and the Bazaar" juga menjadi orang yang mencetuskan istilah _Open Source_. Dia berkata bahwa [Python telah menjadi bahasa pemrograman kesukaannya](http://www.python.org/about/success/esr/). Artikel ini menjadi inspirasi pertama penulis saat belajar Python.
- _Bruce Eckel_ adalah penulis buku 'Thinking in Java' dan 'Thinking in C++' yang terkenal. Dia berkata bahwa tidak ada bahasa yang membuatnya lebih produktif dibanding Python. Dia berkata bahwa Python mungkin satu-satunya bahasa yang fokus untuk memudahkan semuanya untuk programmer. Baca [wawancara lengkapnya](http://www.artima.com/intv/aboutme.html) untuk informasi lebih detail.
- _Peter Norvig_ dikenal sebagai penulis Lisp dan _Director of Search Quality_ di Google (terimakasih untuk Guido van Rossum yang sudah memberitahu). Dia berkata bahwa [menulis Python itu seperti menulis dalam pseudocode](https://news.ycombinator.com/item?id=1803815). Dia berkata bahwa Python akan selalu menjadi bagian penting dari Google. Pembaca juga dapat membuktikan pernyataan ini dengan melihat halaman [Google Jobs](http://www.google.com/jobs/index.html) yang menunjukkan bahwa pengetahuan Python merupakan prasarat untuk _software engineers_.
