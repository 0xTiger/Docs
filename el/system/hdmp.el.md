{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο HDMP - Μορφή αρχείου Windows Heap Dump",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου HDMP και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία HDMP.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Τι είναι ένα αρχείο HDMP;

Το αρχείο HDMP είναι μια ένδειξη ασυμπίεστης μνήμης όταν μια εφαρμογή ή ένα πρόγραμμα διακόπτεται λόγω σφάλματος. Δημιουργείται μόνο από τα Windows XP/Vista και περιέχει μια ένδειξη της κατάστασης της εφαρμογής όταν διακόπηκε. Καθώς δεν είναι συμπιεσμένα, τα αρχεία HDMP καταλαμβάνουν περισσότερο χώρο στο δίσκο σε σύγκριση με τα αρχεία Minidump [MDMP](/el/system/mdmp/) που συμπιέζονται για λόγους αναφοράς.

Οι εφαρμογές που μπορούν να χρησιμοποιηθούν για το **άνοιγμα** ή την ανάλυση αρχείων HDMP περιλαμβάνουν το Microsoft Visual Studio με εργαλεία εντοπισμού σφαλμάτων για Windows.

## Μορφή αρχείου HDMP

Τα αρχεία HDMP αποθηκεύονται σε δίσκο ως δυαδικά αρχεία και δεν παρέχουν κανένα όφελος εάν ανοιχτούν χωρίς κατάλληλες εφαρμογές. Αυτά περιέχουν σχετικά δεδομένα συστήματος που καταγράφηκαν όταν παρουσιάστηκε το σφάλμα.

### Διαφορά μεταξύ των μορφών αρχείων HDMP και MDMP

Τα HDMP είναι αρχεία ένδειξης ασυμπίεστης μνήμης. Αντίθετα, τα MDMP είναι mini dump αρχεία που συμπιέζονται για μείωση του μεγέθους του αρχείου και αποστέλλονται στη Microsoft για αναφορά του προβλήματος.

## Αναφορά ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

