{
  "date": "2022-07-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "IDX – didelio efektyvumo vaizdo kodekas",
  "description": "Sužinokite apie IDX failo formatą ir API, kurios gali kurti ir atidaryti IDX failus.",
  "linktitle": "IDX",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-id-ltx"
}
},
  "lastmod": "2022-07-12"
}

## Kas yra IDX failas?

IDX failas yra subtitrų rodyklės failas, nukreipiantis į subtitrų metaduomenų sąrašą .sub (VobSub subtitrų) faile. Jį sukuria ir naudoja VobSub programinė įranga, leidžianti vartotojams išgauti subtitrus iš DVD ir įrašyti į SUB failą. IDX failuose yra laiko žymos ir baitų poslinkiai, naudojami kiekvienai subtitrai nurodyti. VobSub visada sukuria IDX failą kartu su atitinkamu SUB failu.

## IDX failo formatas – daugiau informacijos

IDX failai generuojami ir išsaugomi kaip paprasto teksto failai, kuriuos galima atidaryti bet kuriame teksto rengyklėje. IDX faile yra informacijos, kurią skaito medijos leistuvai, kad galėtų nuskaityti tokius parametrus kaip subtitrų teksto spalva, kuri bus rodoma ekrane, subtitrų teksto padėtis ekrane.

### IDX subtitrų nustatymai

A typical IDX file stores this metadata information at the start of the file. Subtitle settings begin with a **#**. Timestamps and image references are added after all these subtitle settings and start with **timestamp:**.

## IDX failo formato pavyzdys

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

## Kaip naudoti IDX failą?

Jei turite filmo sub ir IDX failus, galite atkurti šiuos subtitrus kartu su filmu, kuriam jie sukurti. Daugelis programų, tokių kaip VLC, GOM Player, PotPlayer arba PowerDVD, gali įkelti šiuos SUB ir IDX failus ir leisti juos kartu su filmu. Programinės įrangos programos taip pat gali įterpti SUB ir IDX subtitrų failus į [.mkv](/video/mkv/) failus.

## Konvertuoti IDX į SRT

[SRT](/video/srt/) (SubRip failo formatas) yra paprastas subtitrų failas, išsaugotas SubRip failo formatu. Jis dažniau naudojamas, palyginti su VobSub failo formatu. Taigi, jei norite konvertuoti SUB/IDX failus į SRT failo formatą, yra trečiųjų šalių įrankių, kuriuos galima naudoti tam pasiekti. SUB/IDX į SRT keitiklis, pasiekiamas SubtitleTools.com, yra vienas iš tokių įrankių, kuris kaip įvestį priima SUB ir IDX failus ir konvertuoja šiuos VobSub subtitrus į SRT failus.

## Nuorodos

 * [VobSub](https://www.videohelp.com/software/VobSub)
 * [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

