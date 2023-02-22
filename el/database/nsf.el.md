{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "επέκταση", "αρχείο", "μορφή αρχείου", "Τύπος αρχείου βάσης δεδομένων", "Μορφή αρχείου βάσης δεδομένων", "αρχεία βάσης δεδομένων" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου NSF και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία NSF.",
  "title" :"Μορφή αρχείου NSF - Μορφή βάσης δεδομένων Lotus Notes",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Τι είναι ένα αρχείο NSF;

Ένα αρχείο με επέκταση .nsf (Notes Storage Facility) είναι μια μορφή αρχείου βάσης δεδομένων που χρησιμοποιείται από το [λογισμικό IBM Notes](https://en.wikipedia.org/wiki/HCL_Domino), το οποίο στο παρελθόν ήταν γνωστό ως Lotus Notes. Ορίζει το σχήμα για την αποθήκευση διαφορετικών ειδών αντικειμένων όπως email, συναντήσεις, έγγραφα, φόρμες και προβολές. Όλες αυτές οι πληροφορίες περιέχονται σε ένα μόνο αρχείο NSF για επιχειρηματική συνεργασία παρόμοια με ένα αρχείο PST/OST. Μερικές από τις εφαρμογές που μπορούν να ανοίξουν αρχεία NSF περιλαμβάνουν το IBM Lotus Notes και το IBM Domino.

## Προδιαγραφές μορφής αρχείου NSF

Τα αρχεία NSF είναι δυαδικής φύσης και οι προδιαγραφές τους είναι διαθέσιμες από τον Joachim Metz στο [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database% 20file%20format.asciidoc). Σύμφωνα με αυτές τις λεπτομέρειες, ένα αρχείο NSF περιλαμβάνει:

* Κεφαλίδα αρχείου
* Κεφαλίδα βάσης δεδομένων

Επιπλέον, αποτελείται από:

* Superblock
* Μπλοκ περιγραφής κάδου
* Bitmap
* Ρεκόρ Relocation Vector κουβάς
* Κουβάδες περίληψης
* Μη συνοπτικοί κάδοι


### Κεφαλίδα αρχείου NSF

Η κεφαλίδα του αρχείου NSF έχει μέγεθος 6 byte. Αποτελείται απο:

|Μετατόπιση|Μέγεθος|Τιμή|Περιγραφή|
---|---|---|---|
0|2|0x1a 0x00|Υπογραφή|
2|4| |Το μέγεθος της κεφαλίδας της βάσης δεδομένων|

### Κεφαλίδα βάσης δεδομένων

Η κεφαλίδα της βάσης δεδομένων NSD περιέχει τις ακόλουθες επιβεβαιωμένες τιμές.

* Πληροφορίες βάσης δεδομένων
* Αναγνωριστικό βάσης δεδομένων (DBID)
* Πληροφορίες αναπαραγωγής
* Σημαίες buffer πληροφοριών βάσης δεδομένων
* Τίτλος
* Κατηγορίες
* Τάξη
* Κατηγορία σχεδίασης (όνομα προτύπου)
* Ειδικά αναγνωριστικά σημειώσεων
* Γέμισμα
* Πληροφορίες βάσης δεδομένων 2
* Πληροφορίες βάσης δεδομένων 3
* Πληροφορίες βάσης δεδομένων 4
* Πληροφορίες βάσης δεδομένων 5
* Γέμισμα
* Αναγνωριστικό παρουσίας βάσης δεδομένων (DBIID)
* Ιστορικό αντιγραφής

## βιβλιογραφικές αναφορές

* [Μορφή NSF - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)
