{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Αρχείο ZST - Zstandard Compressed File Format",
  "description":"Μάθετε για τη μορφή αρχείου ZST και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία ZST.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-el",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Τι είναι ένα αρχείο ZST;

Ένα αρχείο ZST είναι ένα συμπιεσμένο αρχείο που δημιουργείται με τον αλγόριθμο συμπίεσης Zstandard (zstd). Είναι ένα συμπιεσμένο αρχείο που δημιουργείται με συμπίεση χωρίς απώλειες από τον αλγόριθμο. Τα αρχεία ZST μπορούν να χρησιμοποιηθούν για τη συμπίεση διαφορετικών τύπων αρχείων, όπως βάσεις δεδομένων, συστήματα αρχείων, δίκτυα και παιχνίδια. Το Zstandard διέπεται από το [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) που περιγράφει τον συνολικό μηχανισμό συμπίεσης, τον τύπο μέσων και την κωδικοποίηση περιεχομένου.

## Μορφή αρχείου ZST

Τα αρχεία ZST αποθηκεύονται σε μορφή συμπιεσμένου αρχείου σε δίσκο. Ο μηχανισμός συμπίεσης είναι όπως περιγράφεται από το RFC 8878 που καταργεί το RFC 8478.

## Πλαίσια ZST

Ένα αρχείο ZST αποτελείται από ένα ή περισσότερα πλαίσια. Κάθε πλαίσιο μπορεί να είναι είτε πλαίσιο Zstandard είτε πλαίσιο με δυνατότητα παράβλεψης. Ένα πλαίσιο Zstandard περιέχει συμπιεσμένα δεδομένα, ενώ ένα πλαίσιο με δυνατότητα παράβλεψης περιέχει προσαρμοσμένα μεταδεδομένα χρήστη.

### Zstandard πλαίσιο

Ένα πλαίσιο Zstandard έχει την ακόλουθη δομή.

|Πεδίο|Μέγεθος σε Byte|
---|---|
|Μαγικός_Αριθμός |4 byte|
|Κεφαλίδα_πλαισίου |2-14 byte|
|Data_Block |n byte|
|[Περισσότερα Data_Blocks] ||
|[Content_Checksum] |4 byte|

### Πλαίσιο με δυνατότητα παράβλεψης

Ένα πλαίσιο με δυνατότητα παράβλεψης επιτρέπει την εισαγωγή μεταδεδομένων που ορίζονται από τον χρήστη σε μια ροή συνενωμένων πλαισίων. Η δομή ενός πλαισίου με δυνατότητα παράβλεψης είναι η εξής.

|Μαγικός_Αριθμός |Μέγεθος_πλαισίου |Δεδομένα_χρήστη|
---|---|---|
|4 byte |4 byte |n byte|

## Βιβλιογραφικές αναφορές ##

* [RFC 8878 Zstandard Compression](https://www.rfc-editor.org/rfc/rfc8878)


