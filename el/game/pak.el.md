{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "μορφή αρχείου", "τι είναι ένα αρχείο pak", "αρχείο", "παράδειγμα πακέτου", "Αρχείο πακέτου παιχνιδιών βίντεο", "επέκταση"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε για το αρχείο .pak και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία PAK.",
  "title" :"Μορφή αρχείου PAK- Αρχείο πακέτου βιντεοπαιχνιδιών",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Τι είναι ένα αρχείο PAK;

Ένα αρχείο PAK είναι ένα αρχείο πακέτου που δημιουργήθηκε από διαφορετικά βιντεοπαιχνίδια για την αρχειοθέτηση δεδομένων παιχνιδιού. Ουσιαστικά, είναι μια μορφή αρχείου παιχνιδιού. Αυτό μπορεί να περιλαμβάνει πολλά στοιχεία παιχνιδιού, όπως γραφικά, υφές, ήχους, αντικείμενα, μαζί με άλλα δεδομένα παιχνιδιού. Το αρχείο αποθηκεύεται κυρίως ως αρχείο .zip και μπορεί να εξαχθεί με δημοφιλές λογισμικό αποσυμπίεσης όπως το WinZip και το WinRAR. Παραδείγματα βιντεοπαιχνιδιών που χρησιμοποιούν αρχεία PAK περιλαμβάνουν τα Quake, Hexen, Crysis και Half-Life.

## Μορφή αρχείου PAK - Περισσότερες πληροφορίες

Στις περισσότερες περιπτώσεις, τα αρχεία PAK αποθηκεύονται σε [μορφή αρχείου ZIP](/el/compression/zip/). Ωστόσο, διαφορετικές εφαρμογές ενδέχεται να χρησιμοποιούν διαφορετική μορφή αρχείου για την αποθήκευση αυτών των αρχείων.


## Πώς να ανοίξετε αρχεία PAK;

Μπορείτε να ανοίξετε αρχεία PAK με εφαρμογές όπως το [PakExplorer](https://www.quaketerminus.com/tools.shtml) και το [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- -----------------------**

## Μορφή αρχείου PAK - Αρχείο αντικειμένου Simutrans

Ένα αρχείο με επέκταση .pak είναι μια μορφή αρχείου παιχνιδιού προσομοίωσης μεταφοράς [Simutrans](https://www.simutrans.com/en/). Περιέχει αντικείμενα που χρησιμοποιούνται στην προσομοίωση, όπως γραφικά από χρήστη και περιεχόμενο δεδομένων. Μπορεί να έχει πολλά διαφορετικά αντικείμενα, όπως οχήματα παιχνιδιών, κτίρια, έδαφος κ.λπ. Τα αρχεία PAK δημιουργούνται χρησιμοποιώντας το MakeObject, ένα βοηθητικό πρόγραμμα που μεταγλωττίζει αρχεία .dat και εικόνες .png για τη δημιουργία αυτών των αντικειμένων προσομοίωσης. Το Simutrans επιτρέπει στους παίκτες να τρέξουν ένα επιτυχημένο σύστημα μεταφορών κατασκευάζοντας και διαχειριζόμενοι συστήματα μεταφοράς επιβατών, ταχυδρομείου και εμπορευμάτων μέσω ξηράς

## Πώς να δημιουργήσετε αρχεία PAK;

Η Simutrans έχει παραθέσει δείγματα παραδειγμάτων για τη δημιουργία αρχείων PAK σε λειτουργικά συστήματα Windows και Linux.

### λειτουργικό σύστημα Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## βιβλιογραφικές αναφορές

* https://simutrans-germany.com/wiki/wiki/en_doPak
* https://en.wikipedia.org/wiki/Simutrans
