{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο b6z", "μορφή αρχείου b6z", "τι είναι ένα αρχείο b6z", "αρχείο", "παράδειγμα b6z", "επέκταση αρχείου b6z", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου B6Z - B6ZIP",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου B6Z και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία B6Z.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Τι είναι ένα αρχείο B6Z;

Ένα αρχείο με επέκταση .b6z είναι ένα συμπιεσμένο αρχείο αρχειοθέτησης που δημιουργήθηκε από την εφαρμογή λογισμικού macOS [B6Zip](http://b6zip.com) που χρησιμοποιείται για τη συμπίεση και την αποσυμπίεση αρχείων. Είναι σχετικά νέα μορφή αρχείου που επιτρέπει υψηλότερη αναλογία συμπίεσης. Το B6Z έχει ανοιχτή αρχιτεκτονική και υποστηρίζει μεγέθη αρχείων έως 900000 PB. Υποστηρίζει συμπίεση δεδομένων, ανάκτηση σφαλμάτων και κάλυψη αρχείων. Το βοηθητικό λογισμικό B6Zip είναι διαθέσιμο δωρεάν στο MacOS για το άνοιγμα διαφορετικού τύπου συμπιεσμένων αρχείων, συμπεριλαμβανομένου του B6Z.

## Μορφή αρχείου B6Z

Η μορφή αρχείου B6Z βασίζεται σε ανοιχτή αρχιτεκτονική και παρέχει συμπαγή συμπίεση με τον αλγόριθμο κρυπτογράφησης AES-256. Χρησιμοποιεί το LZMA2 ως προεπιλεγμένη μέθοδο συμπίεσης, αλλά υποστηρίζει και άλλες μεθόδους συμπίεσης ως εξής.

|Μέθοδος|Περιγραφή|
---|---|
|LZMA |Βελτιστοποιημένη έκδοση του αλγορίθμου LZ77|
|LZMA2| Βελτιωμένη έκδοση του LZMA|
|Ξεφούσκωμα| Κανονικός αλγόριθμος LZ77|
|BZip2| Τυπικός αλγόριθμος BWT|
|PPMD| PPMdH του Dmitry Shkarin|

Το βοηθητικό πρόγραμμα B6Zip υποστηρίζει όλα αυτά τα πρότυπα συμπίεσης και είναι εξαιρετικά βελτιστοποιημένο με αποτέλεσμα υψηλή ταχύτητα. Υποστηρίζει εργασία με μορφές αρχείων [ZIP](/el/compression/zip/), [TAR](/el/compression/tar/) και [RAR](/el/compression/rar/). Τα αρχεία B6Z έχουν εφαρμογή τύπου MIME/χ-b6z-συμπιεσμένα.

## βιβλιογραφικές αναφορές

* [B6Zip](http://b6zip.com)

