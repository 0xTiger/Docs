{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - Codec Video Efisiensi Tinggi",
  "description":"Pelajari tentang format file IDX dan API yang dapat membuat dan membuka file IDX.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## Apa itu file IDX?

File IDX adalah file indeks subtitle yang menunjuk ke daftar informasi metadata untuk subtitle di dalam file .sub (VobSub Subtitles). Itu dibuat dan digunakan oleh aplikasi perangkat lunak VobSub yang memungkinkan pengguna mengekstrak subtitle dari DVD dan membuangnya ke file SUB. File IDX berisi stempel waktu dan offset byte yang digunakan untuk menunjuk ke setiap subtitle. VobSub selalu membuat file IDX bersama dengan file SUB yang sesuai.

## Format File BEI - Informasi Lebih Lanjut

File IDX dibuat dan disimpan sebagai file teks biasa yang dapat dibuka di editor teks apa pun. File IDX berisi informasi yang dibaca oleh pemutar media untuk membaca parameter seperti warna teks subtitle untuk ditampilkan di layar, posisi teks subtitle di layar.

### Pengaturan Subtitle BEI

File IDX tipikal menyimpan informasi metadata ini di awal file. Setelan subtitle dimulai dengan **#**. Stempel waktu dan referensi gambar ditambahkan setelah semua setelan subtitel ini dan dimulai dengan **stempel waktu:**.

## Contoh Format File BEI

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## Bagaimana cara menggunakan file IDX?

Jika Anda memiliki file Sub dan IDX untuk sebuah film, Anda dapat memutar subtitle ini bersama dengan film yang dibuatnya. Banyak aplikasi seperti VLC, GOM Player, PotPlayer, atau PowerDVD memiliki kemampuan untuk memuat file SUB dan IDX ini, dan memutarnya bersamaan dengan film. Aplikasi perangkat lunak juga dapat menyematkan file subtitle SUB dan IDX di file [.mkv](/id/video/mkv/).

## Konversikan IDX ke SRT

[SRT](/id/video/srt/) (format file SubRip) adalah file subtitle sederhana yang disimpan dalam format file SubRip. Ini lebih umum digunakan dibandingkan dengan format file VobSub. Jadi, jika Anda ingin mengonversi file SUB/IDX ke format file SRT, tersedia alat pihak ke-3 yang dapat digunakan untuk mencapainya. Konverter SUB/IDX ke SRT, tersedia di SubtitleTools.com adalah salah satu alat yang menggunakan file SUB dan IDX sebagai input dan mengubah subtitle VobSub ini menjadi file SRT.

## Referensi

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

