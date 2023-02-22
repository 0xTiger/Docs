{
  "date" : "2021-04-08",
  "keywords" :[ "αρχείο pkg", "μορφή αρχείου pkg", "τι είναι αρχείο pkg", "αρχείο", "παράδειγμα pkg", "επέκταση αρχείου pkg", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Μορφή αρχείου επεκτάσιμου αρχείου",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου PKG και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία PKG.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Τι είναι ένα αρχείο PKG;

Ένα αρχείο με επέκταση .pkg είναι ένα αρχείο πακέτου εγκατάστασης που χρησιμοποιείται για την εγκατάσταση λογισμικού στο macOS. Εκτός από υπολογιστές Macintosh, χρησιμοποιείται και στο iPhone. Η ενσωματωμένη εφαρμογή εγκατάστασης Apple μπορεί να χρησιμοποιηθεί για την εγκατάσταση των περιεχομένων ενός αρχείου PKG. Ένα αρχείο PKG είναι παρόμοιο με ένα αρχείο MSI που χρησιμοποιείται στο λειτουργικό σύστημα Windows για την εγκατάσταση λογισμικού. Κατά την εγκατάσταση, αυτά τα αρχεία πακέτων μπορούν να καταγράφουν μηνύματα που σας δίνουν μια ιδέα για τα επιπλέον πράγματα που εγκαθίστανται από αυτό το πακέτο.

## Μορφή αρχείου PKG

Τα PKR είναι δυαδικά αρχεία που συμπιέζονται για να μειωθεί το συνολικό μέγεθος του αρχείου. Από το OSX 10.5, η Apple εισήγαγε flat πακέτα με αρχεία μεμονωμένου προγράμματος εγκατάστασης. Αυτές είναι διαφορετικές από τις προηγούμενες μορφές συσκευασίας που ήρθαν ως δέσμες και όχι ως μεμονωμένα αρχεία. Αυτά τα ομαδοποιημένα πακέτα περιείχαν μια δομημένη ιεραρχία καταλόγου που αποθήκευε τα αρχεία με τρόπο που διευκολύνει την ανάκτησή τους μέσω κάποιου αρχείου ευρετηρίου. Η επίπεδη μορφή αρχείου PKG είναι στην πραγματικότητα ένα αρχείο [XAR](/el/compression/xar/) που έχει ένα:

* Κεφαλίδα - Καθορίζει το μέγεθος, το άθροισμα ελέγχου και τις πληροφορίες έκδοσης
* Πίνακας περιεχομένων - Ένα έγγραφο XML που είναι (και πρέπει) να κωδικοποιείται ως UTF-8 και αποθηκεύεται στην αρχή του αρχείου, καθιστώντας εύκολη τη σάρωση μέσω του αρχείου για την εξαγωγή μεμονωμένου αρχείου
* Σωρός - μη δομημένος σωρός δεδομένων που αναφέρονται από το TOC

## βιβλιογραφικές αναφορές

* [Μορφή αρχείου Flat Package](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)
