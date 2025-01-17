{
  "date" : "2021-08-02",
  "keywords" :[ "file pif", "formato file pif", "cos'è un file pif", "file", "esempio pif", "estensione file pif", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file PIF e le API che possono creare e aprire file PIF.",
  "title" :"PIF - File di informazioni sul programma",
  "linktitle" : "PIF",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Che cos'è un file PIF?
Un file PIF è costituito da informazioni utilizzate per determinare come deve essere eseguito un programma basato su MS-DOS. Può anche essere utilizzato come collegamento a un file eseguibile e viene comunemente creato quando l'utente crea un collegamento a un programma DOS o aggiorna le proprietà di un programma. Microsoft Windows riconosce i file PIF come programmi eseguibili e può essere eseguito come altri programmi basati su DOS. I file PIF non sono comunemente usati oggi nel software a causa dell'assenza di applicazioni DOS.

## Formato file PIF
Il file PIF consiste sostanzialmente in un solo blocco di dati che memorizza i parametri necessari per l'esecuzione in TopView. Per opzioni come se la finestra debba essere disattivata o meno al termine del programma, i campi per il titolo della finestra includono la quantità massima e minima di RAM e bitmap. Gli sviluppatori hanno dovuto affrontare il problema che c'erano opzioni aggiuntive che non si applicavano a TopView, quando il sistema è stato adattato per l'uso in Windows. Invece di incorporare le nuove opzioni alla fine del file, creano il file come un file di database che contiene un numero qualsiasi di voci. In questo modo il file consisteva in una serie di aree di intestazione che descrivono quale sistema operativo dovrebbe leggere la sezione e un offset alla sezione successiva. I sistemi leggeranno l'elenco finché non troveranno quello più appropriato. Pertanto, questa teoria ha lasciato un problema di compatibilità con le versioni precedenti. Il file è stato infine riorganizzato con la prima intestazione che appare dopo i dati di partenza, lasciando i primi 253 byte del file nello stesso formato di prima.
### Esempio PIF
Ecco una rappresentazione esadecimale di un file PIF:

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

## Riferimenti

* [File di informazioni sul programma (PIF)](http://justsolve.archiveteam.org/wiki/Program_information_file)
* [File di informazioni sul programma - di Wikipedia ](https://en.wikipedia.org/wiki/Program_information_file)



