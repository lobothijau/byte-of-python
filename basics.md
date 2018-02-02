# Dasar-dasar Python

Hanya mencetak `hello world` tentu tidak cukup bukan? Pembaca tentu ingin melakukan lebih dari hal tersebut - pembaca ingin mengambil beberapa data masukan, mengubahnya serta mendapatkan sesuatu darinya. Kita bisa melakukan hal tersebut di Python menggunakna konstanta dan variabel, dan kita juga akan mempelajari konsep-konsep lainnya di bab ini. 

## Komentar

_Komentar_ adalah semua teks yang berada di sebelah kanan simbol `#` serta berfungsi sebagai catatan yang membantu pembaca program.

Contoh:

```python
print('hello world') # Perhatikan bahwa print adalah sebuah fungsi
```

atau:

```python
# Perhatikan bahwa print adalah sebuah fungsi
print('hello world')
```

Gunakan komentar sebanyak dan sebaik mungkin di program kita untuk:

- menjelaskan asumsi
- menjelaskan keputusan penting
- menjelaskan detail penting
- menjelaskan masalah yang hendak di selesaikan
- menjelaskan masalah yang coba dicegah di progam, dll.

[*Code tells you how, comments should tell you why*](http://www.codinghorror.com/blog/2006/12/code-tells-you-how-comments-tell-you-why.html).

Komentar sangat berguna bagi pembaca program sehingga mereka bisa memahami dengan mudah apa yang dilakukan oleh prgoram tersebut. Ingat, orang tersebut mungkin saja kita sendiri setelah enam bulan kedepan!

## Konstanta Literal/Literal Constants

Sebuah contoh konstanta literal adalah angka seperti `5`, `1.23`, atau sebuah string seperti `'This is a string'` atau `"It's a string!"`.

Data tersebut diberinama literal karena ia bersifat _literal_ - kita menggunakan nilainya secara _literal_ maksudnya secara harfiah persis seperti apa yang ditulis. Angka `2` akan selalu bernilai dua, yaitu angka dua yang kita kenal sehari-hari bukan mewakili jenis data yang lain - ia adalah sebuah _constant_ atau konstanta karena nilainya tidak akan berubah. Oleh karena itu data seperti di atas disebut dengan konstanta literal/_literal constants_.

## Numbers

Numbers umumnya terdiri dari dua tipe - bilangan bulat (integer) dan bilangan riil (float).

Contoh sebuah bilangan bulat adalah `2`. 

Contoh bilangan riil adalah `3.23` dan `52.3E-4`. Notasi `E` mengindikasikan pangkat 10 (exponent). Dalam kasus ini `52.3E-4` berarti `52.3 * 10^-4^`.

> **Catatan Untuk Programmer Berpengalaman**
> 
> Tidak adalah tipe `long` yang terpisah untuk bilangan bulat. Tipe `int` dapat berupa bilangan bulat berukuran berapapun.

## Strings

Sebuah string adalah _deretan_ _karakter_. String secara sederhana hanya kumpulan kata-kata.

Kita akan menggunakan string hampir disetiap program yang kita tulis, jadi perhatikan baik-baik bagian berikut ini.

### Single Quote

Kita dapat membuat string dengan _single quotes_ alias tanda petik satu seperti `'Quote me on this'`.

Spasi dan tab yang ada diantara tanda petik akan ditampilkan apa adanya.

### Double Quotes

String yang ada didalam tanda petik dua bekerja sampa persis dengan string yang menggunakan tanda petik satu. Contohnya adalah `"What's your name?"`.

### Triple Quotes {#triple-quotes}

Kita bisa menulis string lebih dari satu baris menggunakan _triple quotes_ - (`"""` atau `'''`). Kita bebas menggunakan tanda petik satu maupun petik dua didalam _triple quotes_. Contohnya adalah:

```python
'''This is a multi-line string. This is the first line.
This is the second line.
"What's your name?," I asked.
He said "Bond, James Bond."
'''
```

### Strings Bersifat Immutable

Artinya adalah sekali kita membuat sebuah string, kita tidak bisa mengubahnya. Meski terlihat sebagai hal yang buruk, namun nyatanya hal ini tidak lah seperti itu. Kita akan melihat mengapa kekurangan ini tidak akan menghambat program-program yang nantinya akan kita buat. 

> **Catatan Untuk Programmer C/C++**
> 
> Tidak ada tipe data `char` terpisah di Python. Tidak ada kebutuhan untuk itu dan Penulis yakin pembaca pun tidak akan menginginkannya. 

<!-- -->

> **Catatan Untuk Programmer Perl/PHP**
> 
> Ingat bahwa string dengan tanda petik satu maupun dua adalah string yang sama - mereka tidak memiliki perbedaan apapun.

### Method format

Terkadang kita ingin membuat string dan menggabungkannya dengan informasi lain. Disinilah method `format()` akan membantu. 

Simpan baris berikut dalam sebuah file bernama `str_format.py`:

```python
age = 20
name = 'Swaroop'

print('{0} was {1} years old when he wrote this book'.format(name, age))
print('Why is {0} playing with that python?'.format(name))
```

Keluaran:

```
$ python str_format.py
Swaroop was 20 years old when he wrote this book
Why is Swaroop playing with that python?
```

**Bagaimana Cara Kerjanya**

Sebuah string dapat disisipkan data tertentu, method `format` dapat dipanggil untuk menyisipkan data tersebut.

Perhatikan dimana kita menulis `{0}` dan menjadi bagian yang akan menampilkan isi dari variabel `name` yang datang dari argumen pertama method format. Hal yang sama juga terjadi untuk `{1}` yang menampilkan isi variabel `age` di argumen kedua method format. Perhatikan bahwa Python mulai menghitung dari 0 yang mana artinya posisi pertama ada di indeks 0, dan posisi kedua ada di indeks ke 1, dan seterusnya.

Kita juga bisa mendapatkan hasil yang sama menggunakan _string concatenation_:

```python
name + ' is ' + str(age) + ' years old'
```

tapi solusi ini lebih jelek dan mudah mendatangkan kesalahan. Selain itu, konversi dari integer ke string dilakukan secara otomatis oleh method `format` daripada melakukan konversi secara eksplisit (pemanggilan method `str()`). Lalu, saat menggunakan method `format`, kita dapat mengubah isi pesan tanpa berhubungan langsung dengan nama variabel yang dipakai dan juga sebaliknya. 

Juga ingat bahwa angka yang ditulis didalam `{}` bersifat opsional, jadi kita bisa menulisnya sebagai:

```python
age = 20
name = 'Swaroop'

print('{} was {} years old when he wrote this book'.format(name, age))
print('Why is {} playing with that python?'.format(name))
```

hasil yang didapat akan sama dengan program sebelumnya.

Yang dilakukan oleh Python melalui method `format` adalah menyisipkan setiap nilai di dalam argumennya ke tempat yang telah ditentukan. Kita bahkan bisa menambah spesifikasi yang lebih detail seperti:

```python
# decimal (.) precision of 3 for float '0.333'
print('{0:.3f}'.format(1.0/3))
# fill with underscores (_) with the text centered
# (^) to 11 width '___hello___'
print('{0:_^11}'.format('hello'))
# keyword-based 'Swaroop wrote A Byte of Python'
print('{name} wrote {book}'.format(name='Swaroop', book='A Byte of Python'))
```

Keluaran:

```
0.333
___hello___
Swaroop wrote A Byte of Python
```

Karena kita mendiskusikan format, perhatiakn perintah `print` akan selalu menambahkan karakter "baris baru" (`\n`) sehingga memanggil perintah `print` akan mencetaknya dibaris yang berbeda. Untuk mencegah penambahan karakter baris baru, kita harus memberikan parameter `end` kosong sebagai argumen kedua:

```python
print('a', end='')
print('b', end='')
```

Keluarannya adalah:

```
ab
```

Atau kita bisa menentukan `end` dengan spasi kosong:

```python
print('a', end=' ')
print('b', end=' ')
print('c')
```

Keluarannya:

```
a b c
```

### Escape Sequences

Anggaplah kita ingin membuat sebuah string yang didalamnya terdapat simbol petik satu (`'`), bagaimana kita membuat string ini? Contoh string tersebut adalah `"What's your name?"`. Kita tidak dapat menuliskannya sebagai `'What's your name?'` karena Python akan bingung menentukan awal dan akhir string tersebut. Untuk menyelesaikan masalah ini kita bisa menggunakan alat bantu bernama _escape sequence_. Kita menulis petik satu menggunakan `\'` : perhatikan simbol _backslash_. Sekarang, kita bisa menuliskan string tadi sebagai `'What\'s your name?'`.

Cara lain untuk menulis string seperti ini adalah dengan petik dua `"What's your name?"`. Begitu juga saat akan menulis petik dua di dalam string yang menggunakan petik dua, kita harus menggunakan _escape sequence_. Lalu, jika ingin menulis _backslash_ kita juga harus menulisnya dengan _escape sequence_ `\\`.

Bagaimana jika ingin menulis string yang terdiri dari dua baris? Cara pertama ialah menggunakan string petik tiga seperti yang ada di pembahasan [sebelumnya](#triple-quotes) atau menggunakan _escape sequence_ karakter baris baru - `\n` yang mengindikasikan dimulainya baris baru. Contohnya adalah:

```python
'This is the first line\nThis is the second line'
```

_Escape sequence_ lain yang berguna adalah karakter tab: `\t`. Ada banyak lagi _escape sequence_ lain namun ini lah karakter-karakter yang paling sering dipakai. 

Satu hal lagi yang perlu diperhatikan, sebuah string dengan tanda _backslash_ diakhir baris tersebut memberitahu bahwa string itu akan dilanjutkan dibaris berikutnya tanpa menambahkan baris baru. Perhatikan contoh:

```python
"This is the first sentence. \
This is the second sentence."
```

maksudnya sama dengan

```python
"This is the first sentence. This is the second sentence."
```

### Raw String

Jika ingin menulis beberapa string apa adanya tanpa memberikan hal-hal lain seperti _escape sequences_, maka kita perlu membuat string tersebut menjadi _raw string_ dengan memberikan karakter `r` atau `R` di depan string tersebut. Contohny adalah:

```python
r"Newlines are indicated by \n"
```

> **Catatan untuk Pengguna Regular Expression**
> 
> Selalu gunakan raw string saat menggunakan _regular expression_. Jika tidak, beberapa _backwhacking_ mungkin perlu dilakukan. Contoh, _backreferences_ bisa ditulis sebagai `'\\1'` atau `r'\1'`.

## Variabel

Hanya menggunakan konstanta literal saja dapat membuat bosa - kita perlu cara untuk menyimpan informasi lain dan memanipulasinya. Disini lah peran _variabel_ berguna. Variabel, sesuai dengan namanya dapat menyimpan nilai berjenis apapun. Variabel merupakan bagian dari memori komputer kita tempat menyimpan beberapa informasi. Tidak seperti konstanta literal, kita memerlukan sebuah cara untuk mengakses informasi tadi yaitu dengan memberikan nama. 

## Penamaan Variabel

Variabel adalah salah satu contoh _identifiers_. _Identifiers_ adalah nama-nama yang diberikan untuk menandai _sesuatu_. Ada beberapa aturan yang harus diikuti:

- Karakter pertama harus berupa huruf (karakter ASCII uppercase (kapital) maupun lowercase (biasa) atau karakter Unicode) atau berupa _unserscore_ (`_`).
- Karakter-karakter berikutnya dapat berupa huruf, _underscores_, atau angka (0-9).
- Identifier bersifat _case-sensitive_. Contoh, `myname` dan `myName` adalah dua nama yang berbeda. Perhatikan huruf `n` kecil dan `N` besar. 
- Contoh indentifier yang valid adalah `i`, `name_2_3`. Contoh identifier yang tidak valid adalah `2things`, `this is spaced out`, `my-name` dan `>a1b2_c3`.

## Tipe Data

Variabel dapat menyimpan jenis/tipe data yang berbeda-beda.Tipe dasarnya adalah number dan string, yang sudah perna kita bahas. Di bab-babbberikutnya, kita juga bisa membuat tipe data baru dengan  [classes](./oop.md#classes).

## Objek

Ingat, Python akan menganggap semua bagian yang dipakai di dalam program sebagai sebuah _objek_. Sehingga kita tidak mengatakan "sebuah _sesuatu_", tapi kita mengatakan "sebuah _objek_".

> **Catatan untuk Pengguna Object Oriented Programming**:
>
> Python adalah bahasa yang sangat berorientasi objek dalam artian semua adalah sebuah objek termasuk angka, string, dan fungsi. 

Kita akan melihat bagaimana menggunakan variabel bersama dengan konstanta literal. Simpan contoh program di bagian selanjutnya, lalu jalankan. 

## Bagaimana Cara Menulis Program Python

Prosedur standar untuk menyimpan dan menjalankan sebuah program Python adalah sebagai berikut:

### Untuk PyCharm

1. Buka [PyCharm](./first_steps.md#pycharm).
2. Buat fiel baru dengan nama file yang ditentukan.
3. Ketikkan kode program yang diberikan.
4. Klik kanan lalu pilih "run the current file".

NOTE: Setiap kali kita harus memberikan [argumen di command line](./modules.md#modules), Klik dibagian `Run` -> `Edit Configurations` lalu ketikkan argumen yang dimaksud dibagian `Script parameters:` dan klik tombol `OK`:

![PyCharm command line arguments](./img/pycharm_command_line_arguments.png)

### Untuk editor lain

1. Buka editor pilihan.
2. Tulis kode program yang diberikan.
3. Simpan dengan nama yang ditentukan.
4. Jalankan interpreter dengan perintah `python program.py` di terminal.

### Contoh: Menggunakan Variabel dan Konstanta Literal

Tulis dan jalankan program berikut:

```python
# Filename : var.py
i = 5
print(i)
i = i + 1
print(i)

s = '''This is a multi-line string.
This is the second line.'''
print(s)
```

Keluaran:

```
5
6
This is a multi-line string.
This is the second line.
```

**Bagaimana Cara Kerjanyata**

Berikut ini bagaimana cara kerja progra di atas. Pertama, kita menulis sebuah konstanta litera `5` ke dalam variabel `i` menggunakan assignment operator (`=`). Baris ini disebut dengan sebuah _statement_ (perintah) karena ia menyatakan (_states_) sesuatu yang harus dilakukan, dalam kasus ini kita menghubungkan variabel bernama `i` dengan nilai `5`. Selanjutnya, kita mencetak nilai `i` dengan statement `print` yang akan mencetak isi dari variabel tersebut ke layar. 

Lalu kita menambahkan `1` ke dalam nilai yang ada di dalam variabel `i` dan menyimpannya. Kita lalu mencetak isinya dan mendapatkan nilai `6`. 

Berikutnya, kita membuat string dan menyimpannya ke dalam variabel `s` lalu mencetaknya. 

> **Catatan untuk programmer static language**
> 
> Variabel dibuat hanya dengan memberikan suatu nilai disebelahnya. Tidak ada deklarasi atau tipe data yang harus diberikan saat membuatnya. 

## Baris _Logical_ dan _Physical_

Baris fisik (_physical_) adalah baris yang kita _lihat_ saat menulis program. Baris logika (_logical_) adalah baris yang _Python lihat_ sebagai sebuah perintah (_statement_). Python secara implisit mengasumsikan sebuah baris fisik sebagai sebuah baris logika. 

Sebuah contoh baris logika adalah perintah seperti `print 'hello world'` - jika ini adalah satu-satunya perintah di baris tersaebut (seperti yang kita lihat di editor), maka ia juga berupa baris fisik.

Secara implisit, Python akan menyarankan penggunaan satu perintah perbaris untuk membuat kode lebih mudah dibaca. 

Jika ingin menentukan lebih dari satu baris logika di satu baris fisik, maka kita harus secara eksplisit memberitahunya lewat simbol titik koma (`;`). Misalnya:

```python
i = 5
print(i)
```

sama efektifnya dengan

```python
i = 5;
print(i);
```

yang juga sama dengan

```python
i = 5; print(i);
```

dan sama dengan 

```python
i = 5; print(i)
```

Meskipun bisa, penulis *sangat merekomendasikan* untuk menulis *satu baris logika untuk setiap satu baris fisik*. Maksudnya adalah meminimalkan penggunaan titik koma. Penulis bahkan belum pernah menggunakan satu titik koma di sebuah program Python. 

Ada sebuah situasi dimana konsep ini berguna: jika kita memiliki baris kode yang panjang, kita bisa memecahnya menjadi beberapa baris fisik dengan sebuah _backslash_. Teknik ini dinamakan dengan _explicit line joining_:

```python
s = 'This is a string. \
This continues the string.'
print(s)
```

Keluaran:

```
This is a string. This continues the string.
```

Sama juga,

```python
i = \
5
```

tidak berbeda dengan

```python
i = 5
```

Terkadang, ada saat dimana kita tidak perlu sebuah backslash. Kasus ini terjadi saat baris logika memiliki kurang pembuka (`(`, `[` atau `{`) tapi bukan baris penutup. Teknik ini dinamakan *implicit line joining*. Nanti bisa kita lihat saat membuat program menggunakan [list](./data_structures.md#lists).

## Indentasi

_Whitespaces_ atau spasi kosong merupakan bagian yang cukup penting di Python. Bahkan, *spasi kosong dibagian awal baris memiliki arti penting*. Bagian ini dinamakan dengan _indentasi_. Spasi kosong (baik berupa karakter spasi atau tab) di awal baris logika dipakai untuk menentukan level indentasi yang dipakai untuk menentukan pengelompokkan perintah. 

Ini artinya bahwa perintah-perintah yang satu kelompok _harus_ memiliki indentasi yang sama. Kelompok-kelompok tersebut diberi nama *block*. Kita akan melihat bagaimana block memiliki peranan penting di bab-bab berikutnya. 

Satu hal yang perlu diingat adalah indentasi yang tidak sesuai bisa menyebabkan error. Misal:

```python
i = 5
# Error below! Notice a single space at the start of the line
 print('Value is', i)
print('I repeat, the value is', i)
```

Saat program diatas dieksekusi, kita akan mendapat pesan berikut:

```
  File "whitespace.py", line 3
    print('Value is', i)
    ^
IndentationError: unexpected indent
```

Perhatikan bahwa ada satu spasi di bagian awal baris tersebut. Python memberitahu kita bahwa sintaks program ini tidak valid atau dengan kata lain program ini tidak ditulis dengan benar. Maksud dari error ini adalah kita tidak boleh sembarangan membuat blok baru. Kita baru bisa membuat blok baru saat menggunakan [control flow](./control_flow.md#control_flow).

> **Cara melakukan indentasi**
> 
> Gunakan emapt spasi untuk indentasi. Ini adalah rekomendasi resmi dari bahasa pemrograman Python. Editor yang baik akan melakukannya secara otomatis untuk kita. Pastikan untuk menggunakan jumlah spasi yang konsisten untuk indentasi, jika tidak maka program kita tidak akan bisa berjalan atau memiliki tingkah laku yang tidak benar. 

<!-- -->

> **Catatan untuk programmer bahasa pemrogaman static**
> 
> Python akan selalu menggunakan indentasi untuk blok dan tidak akan pernah menggunakan kurung kurawal. Jalankan perintah `from __future__ import braces` untuk penjelasan lebih detail.

## Kesimpulan

Sekrang kita sudah membahas banyak detail-detail bahasa Python dan akhirnya kita bisa lanjut ke bagian yang lebih menarik seperti _control flow statements_. Pastikan sudah cukup bisa memahami konten bab ini.

