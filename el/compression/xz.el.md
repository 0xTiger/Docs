{
  "date" : "2022-01-23",
  "keywords" :[ "αρχείο xz", "μορφή αρχείου", "τι είναι ένα αρχείο xz", "αρχείο", "παράδειγμα xz", "επέκταση αρχείου xz", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο XZ - Συμπιεσμένο αρχείο XZ",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου XZ και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία XZ.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Τι είναι ένα αρχείο XZ;

Το XZ είναι μια συμπιεσμένη μορφή αρχείου που χρησιμοποιεί τον αλγόριθμο συμπίεσης LZMA2. Σχεδιάστηκε ως αντικατάσταση των δημοφιλών μορφών gzip και bzip2 και προσφέρει μια σειρά από πλεονεκτήματα σε σχέση με αυτά τα παλαιότερα πρότυπα. Τα αρχεία XZ υποστηρίζονται καλά σε πολλές πλατφόρμες και μπορούν να αποσυμπιεστούν γρήγορα και εύκολα. Αν και δεν είναι τόσο κοινά όσο τα αρχεία [ZIP](/el/compression/zip/) ή [RAR](/el/compression/rar/), τα αρχεία XZ μπορούν να χρησιμοποιηθούν για την αποθήκευση μεγάλων ποσοτήτων δεδομένων χωρίς να θυσιάζεται η ποιότητα συμπίεσης. Εάν χρειάζεται να συμπιέσετε ή να αποσυμπιέσετε μεγάλα αρχεία, αξίζει να λάβετε υπόψη την επέκταση αρχείου XZ.

## Μορφή αρχείου XZ

Τα αρχεία XZ δημιουργούνται και αποθηκεύονται ως δυαδικά αρχεία στο δίσκο. Χρησιμοποιεί τον αλγόριθμο LZMA για τη συμπίεση δεδομένων και μπορεί να επιτύχει αναλογία συμπίεσης έως και 50%. Τα αρχεία XZ χρησιμοποιούνται συνήθως για διανομές λογισμικού και αρχεία αντιγράφων ασφαλείας. Μπορούν να αποσυμπιεστούν χρησιμοποιώντας το βοηθητικό πρόγραμμα XZ, το οποίο περιλαμβάνεται στις περισσότερες διανομές Linux.

## Αποσυμπιέστε τα αρχεία XZ σε Linux/Unix

Για να αποσυμπιέσετε αρχεία XZ, εγκαταστήστε πρώτα το πακέτο «xz-utils»:
```
$ sudo apt-get install xz-utils
```

Χρησιμοποιήστε την εντολή "unxz" για να εξαγάγετε αρχεία .xz:
```
$ unxz compressed_xz_file.xz
```

ή χρησιμοποιώντας με την επιλογή --decompress του XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## βιβλιογραφικές αναφορές

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)
