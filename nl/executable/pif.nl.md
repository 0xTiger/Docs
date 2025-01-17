{
  "date" : "2021-08-02",
  "keywords" :[ "pif-bestand", "pif-bestandsformaat", "wat is een pif-bestand", "bestand", "pif-voorbeeld", "pif-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over PIF-bestandsindeling en API's die PIF-bestanden kunnen maken en openen.",
  "title" :"PIF - Programma-informatiebestand",
  "linktitle" : "PIF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Wat is een PIF-bestand?
Een PIF-bestand bestaat uit informatie die wordt gebruikt om te bepalen hoe een op MS-DOS gebaseerd programma moet worden uitgevoerd. Het kan ook worden gebruikt als een snelkoppeling van een uitvoerbaar bestand en wordt vaak gemaakt wanneer de gebruiker een snelkoppeling naar een DOS-programma maakt of de eigenschappen van een programma bijwerkt. Microsoft Windows herkent de PIF-bestanden als uitvoerbare programma's en kan worden uitgevoerd als andere op DOS gebaseerde programma's. De PIF-bestanden worden tegenwoordig niet vaak gebruikt in software vanwege het ontbreken van DOS-toepassingen.

## PIF-bestandsindeling
Het PIF-bestand bestaat in feite uit slechts één gegevensblok waarin de parameters zijn opgeslagen die nodig zijn om onder de TopView uit te voeren. Voor schakelaars zoals of het venster al dan niet moet worden uitgeschakeld wanneer het programma eindigt, bevatten de velden voor de venstertitel de maximale en minimale hoeveelheid RAM en bitmaps. De ontwikkelaars hadden het probleem dat er extra schakelaars waren die niet van toepassing waren op TopView, toen het systeem werd aangepast voor gebruik onder Windows. In plaats van de nieuwe schakelaars aan het einde van het bestand op te nemen, maken ze het bestand als een databasebestand dat een willekeurig aantal vermeldingen bevat. Op deze manier bestond het bestand uit een aantal koptekstgebieden die beschrijven welk besturingssysteem de sectie zou moeten lezen, en een verschuiving naar de volgende sectie. Systemen zullen de lijst lezen totdat ze de meest geschikte hebben gevonden. Daarom liet deze theorie een probleem van achterwaartse compatibiliteit achter. Het bestand werd uiteindelijk opnieuw gerangschikt met de eerste koptekst die verscheen na de startgegevens, waardoor de eerste 253 bytes van het bestand in hetzelfde formaat bleven als voorheen.
### PIF Voorbeeld
Hier is een hexadecimale weergave van een PIF-bestand:

```
0000000: 0078 494e 5354 414c 4c20 2020 2020 2020  .xINSTALL       
0000010: 2020 2020 2020 2020 2020 2020 2020 2020                  
0000020: 8002 0000 433a 5c74 656d 705c 7465 6d70  ....C:\temp\temp
0000030: 335c 494e 5354 414c 4c2e 4558 4500 0000  3\INSTALL.EXE...
0000040: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000050: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000060: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000070: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000080: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000090: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00000a0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00000b0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00000c0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00000d0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00000e0: 0000 0000 0000 0100 ff19 5000 0007 0000  ..........P.....
00000f0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000100: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000110: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000120: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000130: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000140: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000150: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000160: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000170: 004d 4943 524f 534f 4654 2050 4946 4558  .MICROSOFT PIFEX
0000180: 0087 0100 0071 0157 494e 444f 5753 2033  .....q.WINDOWS 3
0000190: 3836 2033 2e30 0005 029d 0168 0080 0200  86 3.0.....h....
00001a0: 0064 0032 00ff ff00 00ff ff00 0002 1002  .d.2............
00001b0: 001f 0000 0000 0000 0000 0000 0000 0000  ................
00001c0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00001d0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00001e0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00001f0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000200: 0000 0000 0057 494e 444f 5753 2056 4d4d  .....WINDOWS VMM
0000210: 2034 2e30 00ff ff1b 02ac 0100 0000 0000   4.0............
0000220: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000230: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000240: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000250: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000260: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000270: 0000 0050 4946 4d47 522e 444c 4c00 0000  ...PIFMGR.DLL...
0000280: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000290: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00002a0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00002b0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00002c0: 0000 0000 0002 0000 0000 0000 0000 0000  ................
00002d0: 0032 0001 0000 0000 0000 0000 0000 0001  .2..............
00002e0: 0000 0005 0019 0003 00c8 00e8 0302 000a  ................
00002f0: 0001 0000 0000 0000 001c 0000 0000 0000  ................
0000300: 0008 000c 0054 6572 6d69 6e61 6c00 0000  .....Terminal...
0000310: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000320: 0000 0000 004c 7563 6964 6120 436f 6e73  .....Lucida Cons
0000330: 6f6c 6500 0000 0000 0000 0000 0000 0000  ole.............
0000340: 0000 0000 0000 0003 0000 0050 0019 0080  ...........P....
0000350: 022c 018c 0267 0116 0000 0001 00ff ffff  .,...g..........
0000360: ffff ffff ffae 0626 013a 098d 0200 0000  .......&.:......
0000370: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000380: 0000 0000 0000 0000 0000 0000 0000 0000  ................
0000390: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00003a0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00003b0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00003c0: 0000 0000 0001 00                        .......
```

## Referenties

* [Programma-informatiebestand (PIF)](http://justsolve.archiveteam.org/wiki/Program_information_file)
* [Programma-informatiebestand - door Wikipedia](https://en.wikipedia.org/wiki/Program_information_file)



