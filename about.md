# Appendix: Colophon {#colophon}

Hampir semua perangkat lunak yang Penulis gunakan untuk menulis buku ini adalah [FLOSS](./floss.md#floss).

## Birth of the Book

Di draft pertama buku ini, Penulis menggunakan Linux Red Hat 9.0 sebagai dasar buku ini dan di draft yang keenam, Penulis menggunakan Linux Fedora Core 3.

Pada awalnya Penulis menggunakan KWord untuk menulis buku ini (seperti yang dijelaskan dibagian  [history lesson](./revision_history.md#history-lesson))

## Teenage Years

Lalu, Penulis merubahnya dengan menggunakan DocBook XML dan Kate tapi ternyata terlalu merepotkan. Jadi, Penulis putuskan bahwa OpenOffice merupakan solusi terbaik karena sudah ada formatting dan bisa membuat file PDF, namun ia tidak mampu membuat dokumen HTML yang bagus. 

Akhirnya, Penulis menemukan XEmacs dan Penulis menulis ulang buku ini dari awal dengan DocBOok XML (lagi) setelah Penulis putuskan bahwa format ini merupakan solusi jangka panjang. 

Di draft keenam, Penulis putuskan untuk menggunakan Quanta+ untuk semua editing. Standar stylesheet XSL yang ada di Linux Fedora Core 3 dipakai. Namun, Penulis harus membuat dokumen CSS untuk memberikan warna dan style halaman HTML. Penulis juga membuat sebuah crude lexical analyzer, dalam bahasa Python tentu saja, yang secara otomatis akan memberikan syntax highlighting untuk semua kode program. 

Untuk draft ketujuh, penulis menggunakan [MediaWiki](http://www.mediawiki.org). Penulis awalnya melakukan proses edit secara online dan pembaca dapat membaca/mengedit/mendiskusikan buku langsung di website wiki langsung, namun Penulis berakhir dengan mengurus spam dibanding menulis.

Di draft yang kedelapan, Penulis menggunakan [Vim]({{ book.vimBookUrl }}), [Pandoc](http://johnmacfarlane.net/pandoc/README.html), dan Mac OS X.

Di draft kedelapan, Penulis berubah menggunakan [AsciiDoc format](http://asciidoctor.org/docs/what-is-asciidoc/) dan memakai [Emacs 24.3](http://www.masteringemacs.org/articles/2013/03/11/whats-new-emacs-24-3/),
[tomorrow theme](https://github.com/chriskempson/tomorrow-theme),
[Fira Mono font](https://www.mozilla.org/en-US/styleguide/products/firefox-os/typeface/#download-primary) and [adoc-mode](https://github.com/sensorflo/adoc-mode/wiki) untuk menulisnya.

## Now

2016: Penulis letih dengan masalah rendering di AsciiDoctor, seperti `++` di `C/C++` akan menghilang dan sulit untuk mencari cara menyelesaikan masalah tersebut. Selain itu, Penulis juga sudah mulai enggan untuk mengedit dalam format Asciidoc yang kompleks. 

Untuk draft yang kesepuuh, Penulis ganti menggunakan format Markdown + [GitBook](https://www.gitbook.com), dengan editor [Spacemacs editor](http://spacemacs.org).

## About the Author

Lihat {{ book.authorUrl }}
