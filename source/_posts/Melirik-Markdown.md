---
title: Melirik Markdown
description: "Pengantar Markdown, sebuah bahasa pemformatan teks sekaligus aplikasi pengubah teks ke html."
excerpt: "Markdown adalah dua hal: sintak penyuntingan teks biasa, dan sekaligus aplikasi pengubah format teks biasa menjadi HTML."
categories:
  - Dokumen
tags:
  - markdown
  - teks biasa
  - tulis-menulis
  - pengantar
---

## Apa itu Markdown

Markdown adalah alat untuk mengubah teks biasa ke HTML yang lebih ditujukan bagi para penulis _web_. Markdown membuat aktivitas tulis-menulis mampu dikerjakan memakai media teks biasa yang mudah disunting dan _gampang_ dibaca, selanjutnya Markdown mengubah teks biasa tersebut menjadi dokumen berjenis XHTML (atau HTML) yang terstruktur dan valid[^1].

  [^1]: Diterjemahkan dari [Daring Fireball](https://daringfireball.net/projects/markdown/#Introduction).

Dengan demikian, Markdown adalah dua hal:
1. Sintak pemformatan teks biasa;
2. Perangkat lunak (aplikasi) yang mengubah format teks biasa ke HTML.


Konsep utama perancangan sintak Markdown adalah agar semaksimal mungkin mampu dibaca dengan baik, tanpa terlihat telah dimarkahi atau disuting dengan beragam format penulisan tertentu.

Markdown​ diciptakan oleh seorang pengarang, penulis blog, dan sekaligus perancang [UI][] bernama [John Gruber][jb]. Berkolaborasi dengan [Aaron Swartz](as) dalam merancang sintaknya, versi perdana Markdown akhirnya dirilis pada tanggal 19 Maret 2004, kemudian rilis terakhir versi `1.0.1` diumumkan pada tanggal 7 Desember 2004.

  [jb]: https://en.wikipedia.org/wiki/John_Gruber
  [ui]: https://id.wikipedia.org/wiki/Antarmuka_pengguna
  [as]: https://en.wikipedia.org/wiki/Aaron_Swartz

## Sintak Markdown

Menulis memakai sintak Markdown tidaklah sesulit memahami penjabaran mengenai sintak-sintak yang akan dibahas disini, baiknya, pada setiap penjabaran hendaknya dipahami sembari di praktekkan.

Untuk mempraktekkannya, silahkan gunakan aplikasi penyunting teks berformat Markdown yang menurut saya telah tersedia di berbagai jenis Gawai, beberapa aplikasi yang dapat saya temukan adalah:

**Windows, Mac, dan Linux**:  
[Haroopad][hp], [Typora][tp], dan [Markdown Plus][ms] serta [MarkPad][mp].

  [hp]: http://pad.haroopress.com/
  [mp]: http://code52.org/DownmarkerWPF
  [tp]: https://typora.io/
  [ms]: https://tylingsoft.com/markdown-plus/

**iOS**:  
[Editorial][et], [Ulysses][us] dan [1write][1w].

  [et]: https://itunes.apple.com/us/app/editorial/id673907758?mt=8&uo=4&at=10l6nh&ct=ms_inline
  [us]: https://itunes.apple.com/us/app/ulysses/id950335311?mt=8&uo=4&at=10l6nh&ct=ms_inline
  [1w]: http://1writerapp.com

**Android**:  
  [MarkdownX][mx], [Epsilon Notes][es], dan [JotterPad][jp].

  [mx]: https://play.google.com/store/apps/details?id=com.ryeeeeee.markdownx
  [es]: https://play.google.com/store/apps/details?id=com.ekartoyev.enotes
  [jp]: https://play.google.com/store/apps/details?id=com.jotterpad.x

### Judul atau Tajuk

Membuat Judul dapat dilakukan dengan dua cara, yaitu memakai pemarkahan bergaya _Setext_ atau dengan mengadopsi gaya pemarkahan ala _atx_.

#### Judul Ala Setext

Judul ala Setext hanya mencakup dua tingkatan Judul, yaitu "Judul Utama" dan "Sub-judul". Dalam format HTML, kedua tingkatan judul tersebut disebut dengan H1 `<h1>` dan H2 `<h2>`.

Judul utama dibuat dengan menyisipkan tanda sama dengan `=` tepat di bawah kata atau kalimat, sedangkan Sub-judul dibuat dengan memanfaatkan tanda hubung `-`.

Contohnya:

```markdown
Judul Utama atau H1
===================

Paragraf

Sub-judul atau H2
-----------------

Paragraf
```

Format HTML yang dihasilkan:

```html
<h1>Judul Utama atau H1</h1>

<p>Paragraf</p>

<h2>Sub-judul atau H2</h2>

<p>Paragraf</p>
```

#### Judul Ala atx

Dengan memakai judul ala **atx** kita dapat membuat hingga 6 tingkatan Judul, yaitu H1 `<h1>` hingga H2 `<h2>`. Judul ala atx ditandai dengan tanda pagar `#` diikuti dengan `spasi` di awal kata atau kalimat, jumlah tanda pagar `#` mengindikasikan tingkatan judul tersebut.

Misalnya:
```markdown
# Judul Utama atau H1

## Sub-judul pertama atau H2

### Sub-judul kedua atau H3

#### Sub-judul ketiga atau H4

##### Sub-judul keempat atau H5

###### Sub-judul kelima atau H6
```

Format HTML yang dihasilkan:
```html
<h1>Judul Utama atau H1<h1>

<h2>Sub-judul pertama atau H2<h2>

<h3>Sub-judul kedua atau H3<h3>

<h4>Sub-judul ketiga atau H4<h4>

<h5>Sub-judul keempat atau H5<h5>

<h6>Sub-judul kelima atau H6<h6>
```

### Paragraf dan Ganti Baris

#### Paragraf

Sebuah paragraf, sederhananya adalah rangkaian kata atau kalimat yang dipisahkan dengan satu atau lebih baris kosong. Setiap baris yang terlihat kosong, meskipun memuat `spasi` dan/atau `tab`, tetap dinamakan sebagai baris kosong.
           
Mudahnya, untuk membuat paragraf, Kita hanya perlu menekan tombol `Enter` paling tidak sebanyak dua kali.

Berikut ini contoh penulisannya:
```css
Paragraf 1, lorem ipsum dolor sit/*Enter*/
amet, bla bla bla…/*Enter*/
/*Enter*/
Paragraf 2, mauris maximus/*Enter*/
ultrices dui sed faucibus. Bla bla bla…/*Enter*/
/*Enter*/
/*Enter*/
Paragraf 3, Quisque vehicula/*Enter*/
sollicitudin lectus/*Enter*/
efficitur. Bla bla bla…
```

Kemudian Markdown akan mengubahnya  dalam format HTML menjadi:

```html
<p>Paragraf 1, lorem ipsum dolor sit amet, bla bla bla…</p>
<p>Paragraf 2, mauris maximus ultrices dui sed faucibus. Bla bla bla…</p>
<p>Paragraf 3, Quisque vehicula sollicitudin lectus efficitur. Bla bla bla…</p>
```

#### Ganti Baris

Untuk memulai garis baru atau berganti baris dapat dilakukan dengan menyisipkan setidaknya dua `spasi` di akhir kata atau kalimat.

Contohnya:
```css
Lalu bagaimana/* Tanpa spasi */
jika saya hanya ingin memulai  /* 2 spasi di akhir kalimat */
baris baru /* Spasi tunggal */
atau berganti baris     /* 5 Spasi tunggal */
dalam sebuah paragraf.
```

Format HTML yang dihasilkan:
```html
<p>Lalu bagaimana jika saya hanya ingin memulai<br>baris baru atau berganti baris<br>dalam sebuah paragraf.</p>
```

### Teks Tebal dan Miring

Teks tebal dan/atau miring biasanya digunakan untuk memberikan penekanan pada teks tersebut, dalam format html teks tebal ditandai dengan _Strong_ `<strong>` dan tanda _Emphasis_ `<em>` untuk teks miring.

Teks miring dibuat dengan melingkupi teks tersebut memakai sebuah tanda bintang `*` atau sebuah tanda garis bawah `_`, sedangkan teks tebal dibuat dengan menggandakan kedua tanda tersebut.

Misalnya:
```markdown
Teks *miring* dan _sebaris kalimat panjang yang juga miring_.

Teks **tebal** dan sebaris __kalimat panjang yang juga tebal__.
```

Format HTML yang dihasilkan:

```html
<p>Teks <em>miring</em> dan <em>sebaris kalimat panjang yang juga miring</em>.</p>

<p>Teks <strong>tebal</strong> dan sebaris <strong>kalimat panjang yang juga tebal</strong>.</p>
```

### Kutipan

Membuat sebuah kutipan dapat dilakukan dengan cara menambahkan tanda "lebih dari" `>` di awal baris.

Misalnya:
```markdown
> Beri aku 1.000 orang tua, niscaya akan kucabut semeru dari akarnya. Beri aku 10 pemuda niscaya akan kuguncangkan dunia.
>
> _Soekarno_
```

Menghasilkan format html:
```html
<blockquote>
<p>Beri aku 1.000 orang tua, niscaya akan kucabut semeru dari akarnya. Beri aku 10 pemuda niscaya akan kuguncangkan dunia.</p>
<p><em>Soekarno</em></p>
</blockquote>
```

### Daftar atau Senarai

#### Daftar Bertanda Titik

Daftar bertanda titik dalam format html disebut dengan _unordered list_ yang secara harfiah berarti daftar tidak berurutan, daftar model ini dibuat dengan memanfaatkan tanda bintang `*` atau tanda hubung `-`, dan atau tanda tambah `+`.

Misalnya:
```markdown
* Biru
* Hijau
* Merah
```

atau
```markdown
- Biru
- Hijau
- Merah
```

dan atau
```markdown
+ Biru
+ Hijau
+ Merah
```

Ketiganya menghasilkan format html yang sama:
```html
<ul>
  <li>Biru</li>
  <li>Hijau</li>
  <li>Merah</li>
</ul>
```

#### Daftar Bernomor

Daftar bernomor atau berurutan (&shy;_ordered list_&shy; dibuat dengan memakai angka biasa yang diiringi dengan tanda titik.

Misalnya:

```markdown
1. Nomor 1
2. Nomor 2
3. Nomor 3
```

Menghasilkan format html:
```
<ol>
<li>Nomor 1</li>
<li>Nomor 2</li>
<li>Nomor 3</li>
</ol>
```

#### Daftar Multi-paragraf


Jika Kita ingin menambahkan beberapa paragraf pada deretan daftar, yang perlu kita lakukan adalah menyisipkan baris kosong setelah sebuah daftar, lalu menuliskan sebaris paragraf yang _diindentasi_ dengan 4 spasi maka paragraf tersebut akan termuat dalam daftar tersebut.

Misalnya;
```markdown
* Daftar Merah

    Dengan beberapa paragraf

* Kelanjutan Daftar Merah
```

Format html yang dihasilkan:
```html
<ul>
  <li>
    <p>Daftar Merah</p>
    <p>Dengan beberapa paragraf</p>
  </li>
  <li>
    <p>Kelanjutan Daftar Merah</p>
  </li>
</ul>
```

### Tautan dan Gambar

Penyisipan alamat tautan dapat dilakukan secara inline (&shy;_inline_&shy;) atau serupa penyisipan refrensi (&shy;_reference_&shy;), pada kedua cara tersebut tanda kurung siku `[…]` digunakan untuk membatasi teks yang hendak dijadikan sebagai tautan.

#### Tautan _Inline_ (langsung)

Pada tautan _inline_ (langsung), alamat tautan diletakkan dalam tanda kurung `(…)` dan disisipkan secara langsung tepat setelah teks yang hendak dijadikan sebagai tautan.

> **Contoh**:

> Bentuk Markdown:  
```markdown
[teks](http://alamat-tautan.com)
```
> Rupa Html:
```html
<a href="http://alamat-tautan.com">teks</a>
```

Atribut _title_ atau keterangan tambahan pada tautan dapat Kita sisipkan setelah 'alamat tautan', dipisahkan dengan spasi dan melingkupinya memakai tanda petik `"…"`.

> **Contoh**:

> Bentuk Markdown:  
```markdown
[teks](http://alamat-tautan.com "title atau keterangan tambahan")
```

> Rupa Html:
```html
<a href="http://alamat-tautan.com" title="title atau keterangan tambahan">teks</a>
```

#### Tautan _Reference_ (Refrensi)

Saat memakai tautan bergaya _reference_ (refrensi), Kita dapat merujukkan tautan yang kita buat dengan nama tertentu, lalu meletakkan 'alamat tautan' pada bagian manapun dokumen yang tengah Kita kerjakan.

Nama tautan yang digunakan sebagai rujukan tidak memperdulikan antara huruf kapital dengan huruf kecil (&shy;_**not** case sensitive_&shy;) dan dapat berupa huruf, angka, dan spasi.

Contoh:

```markdown
[**Candi Badut**][1] adalah sebuah
[candi][ ] yang terletak di kawasan
Tidar, di bagian barat kota Malang.

[1]: https://id.wikipedia.org/wiki/Candi_Badut "Candi Badut" <!--- Memakai angka --->
[ ]: https://id.m.wikipedia.org/wiki/Candi "Pengertian Candi" <!--- Memakai spasi --->

Secara administratif candi badut
terletak di Kelurahan Karang Besuki,
Kecamatan [Sukun][], [Kota
Malang][k], [Jawa Timur][ 1aA@].

    <!--- # Indentasi dengan dua spasi # --->
  [sukun]: https://id.wikipedia.org/wiki/Dau,_Malang "Sukun" <!--- Mengabaikan besar kecilnya huruf --->
  [k]: https://id.wikipedia.org/wiki/Kota_Malang "Kota Malang" <!--- Memakai huruf --->
  [ 1aA@]: https://id.wikipedia.org/wiki/Jawa_Timur "Provinsi Jawa Timur" <!--- Campuran --->
```

Format html yang dihasilkan:
```html
<p><a href="https://id.wikipedia.org/wiki/Candi_Badut" title="Candi Badut"><strong>Candi Badut</strong></a> adalah sebuah <a href="https://id.m.wikipedia.org/wiki/Candi" title="Pengertian Candi">candi</a> yang terletak di kawasan
Tidar, di bagian barat kota Malang.</p>
<p>Secara administratif candi badut
terletak di Kelurahan Karang Besuki, Kecamatan <a href="https://id.wikipedia.org/wiki/Dau,_Malang" title="Sukun">Sukun</a>, <a href="https://id.wikipedia.org/wiki/Kota_Malang" title="Kota Malang">Kota
Malang</a>, <a href="https://id.wikipedia.org/wiki/Jawa_Timur" title="Provinsi Jawa Timur">Jawa Timur</a>.</p>
```

#### Gambar

Cara menyisipkan gambar dapat dikatakan menyerupai sintak penyisipan tautan, perbedaannya hanya terletak pada penambahan tanda seru `!` di awal sintaknya.

**_Inline_**:
```markdown
![teks alternatif](/alamat/menuju/gambar.jpg "Title atau keterangan tambahan")
```

**_Reference_**:
```markdown
![teks alternatif][nama refrensi]

[nama refrensi]: /alamat/menuju/gambar.jpg "Title atau keterangan tambahan"
```

Kedua contoh di atas akan menghasilkan format html yang sama:
```html
<img src="/alamat/menuju/gambar.jpg" alt="teks alternatif" title="Title atau keterangan tambahan" />
```

