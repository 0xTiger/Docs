{
  "date": "2022-07-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "IDX - High Efficiency Video Codec",
  "description": "Lær om IDX-filformat og API'er, der kan oprette og åbne IDX-filer.",
  "linktitle": "IDX",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-id-dax"
}
},
  "lastmod": "2022-07-12"
}

## Hvad er en IDX fil?

En IDX-fil er en undertekstindeksfil, der peger på listen over metadataoplysninger for undertekster inde i en .sub (VobSub Subtitles) fil. Det er oprettet og brugt af VobSub-softwareapplikationen, der lader brugere udtrække undertekster fra dvd'er og dumpe i en SUB-fil. IDX-filer indeholder tidsstempler og byte-forskydninger, der bruges til at pege på hver enkelt undertekst. VobSub opretter altid en IDX-fil sammen med den tilsvarende SUB-fil.

## IDX-filformat - flere oplysninger

IDX-filer genereres og gemmes som almindelige tekstfiler, der kan åbnes i enhver teksteditor. En IDX-fil indeholder information, som læses af medieafspillerne for at læse parametre, såsom farven på undertekstteksten, der skal vises på skærmen, underteksttekstens position på skærmen.

### IDX-undertekstindstillinger

A typical IDX file stores this metadata information at the start of the file. Subtitle settings begin with a **#**. Timestamps and image references are added after all these subtitle settings and start with **timestamp:**.

## Eksempel på IDX-filformat

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

## Hvordan bruger man IDX fil?

Hvis du har Sub- og IDX-filerne til en film, kan du afspille disse undertekster sammen med den film, som disse er lavet til. Mange applikationer såsom VLC, GOM Player, PotPlayer eller PowerDVD har mulighed for at indlæse disse SUB- og IDX-filer og afspille disse sammen med filmen. Softwareapplikationer kan også indlejre SUB- og IDX-undertekstfiler i [.mkv](/video/mkv/)-filer.

## Konverter IDX til SRT

[SRT](/video/srt/) (SubRip-filformat) er en simpel undertekstfil, der er gemt i SubRip-filformatet. Det er mere almindeligt brugt sammenlignet med VobSub-filformatet. Hvis du vil konvertere SUB/IDX-filer til SRT-filformat, er der 3. parts værktøjer tilgængelige, som kan bruges til at opnå dette. SUB/IDX til SRT-konverter, tilgængelig på SubtitleTools.com er et sådant værktøj, der tager SUB- og IDX-filer som input og konverterer disse VobSub-undertekster til SRT-filer.

## Referencer

 * [VobSub](https://www.videohelp.com/software/VobSub)
 * [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)
