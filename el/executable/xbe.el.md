{
  "date" : "2021-08-31",
  "keywords" :[ "αρχείο xbe", "μορφή αρχείου xbe", "τι είναι ένα αρχείο xbe", "αρχείο", "παράδειγμα xbe", "επέκταση αρχείου xbe", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε σχετικά με τη μορφή αρχείου XBE και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία XBE.",
  "title" :"XBE - Αρχείο πακέτου εφαρμογών iOS",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## Τι είναι ένα αρχείο XBE;
Ένα αρχείο με επέκταση .xbe είναι μια εκτελέσιμη εφαρμογή από έναν δίσκο βιντεοπαιχνιδιών Xbox. Τα αρχεία XBE είναι τα κύρια αρχεία που εκτελούνται στο σύστημα Xbox και δεν υποτίθεται ότι ανοίγουν συνήθως σε υπολογιστή, αλλά μπορούν να ανοίξουν σε υπολογιστή χρησιμοποιώντας ένα πρόγραμμα εξομοίωσης Xbox. Αυτά τα αρχεία δημιουργούνται συνήθως από προγραμματιστές παιχνιδιών και στη συνέχεια υπογράφονται από τη Microsoft. Η δομή του αρχείου είναι παρόμοια με τα αρχεία PE των Windows, αλλά εφαρμόζονται ορισμένες σημαντικές αλλαγές σύμφωνα με τις ρυθμίσεις του XBox για να είναι δυνατή η εκτέλεση στο XBox.

## Μορφή αρχείου XBE
Το αρχείο XBE αποτελείται από μια κεφαλίδα εικόνας, μια συλλογή κεφαλίδων ενότητας, ένα πιστοποιητικό, δεδομένα τοπικής αποθήκευσης νήματος, μια συλλογή εκδόσεων βιβλιοθήκης, bitmap της Microsoft και τις ενότητες που περιέχουν τον κώδικα και τους πόρους.

### Κεφαλίδα εικόνας
Η κεφαλίδα εικόνας περιλαμβάνει τις πληροφορίες που εξηγούν πού βρίσκονται τα άλλα στοιχεία του εκτελέσιμου αρχείου και πώς πρέπει να αντιμετωπίζεται και να φορτώνεται το runnable.

### Πίνακας TLS
Ο Πίνακας TLS αποτελείται από όλες τις πληροφορίες που χρειάζεται το XBE για τη σωστή ρύθμιση της τοπικής αποθήκευσης νημάτων. Είναι βασικά μοναδικός στον Κατάλογο TLS που βρίσκεται στα αρχεία PE32 και μπορεί να αντιγραφεί απευθείας από εκεί. Αυτός ο πίνακας μπορεί να παραλειφθεί, εάν το αρχείο XBE δεν χρησιμοποιεί τοπική αποθήκευση νήματος και το αντίστοιχο πεδίο στην κεφαλίδα της εικόνας να μηδενιστεί.

| Offset | Μέγεθος | Όνομα | Περιγραφή |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Έναρξη ακατέργαστων δεδομένων | Απόλυτη (δηλαδή όχι RVA) διεύθυνση έναρξης των δεδομένων μεταβλητής TLS στην εικόνα του προγράμματος. |
| 0x0004 | 0x0004 | Τέλος ακατέργαστων δεδομένων | Απόλυτη (δηλαδή όχι RVA) διεύθυνση του τέλους των δεδομένων μεταβλητής TLS στην εικόνα του προγράμματος. |
| 0x0008 | 0x0004 | Διεύθυνση Ευρετηρίου | Απόλυτη (δηλαδή όχι RVA) διεύθυνση της μεταβλητής Index TLS. |
| 0x000C | 0x0004 | Διεύθυνση Επανακλήσεων | Απόλυτη (δηλαδή όχι RVA) διεύθυνση του πίνακα συναρτήσεων επανάκλησης TLS με μηδενικό τερματισμό. |
| 0x0010 | 0x0004 | Μέγεθος Zero Fill | Ο αριθμός των byte που ακολουθούν τα ανεπεξέργαστα δεδομένα που θα πρέπει να μηδενιστεί στη μνήμη. |
| 0x0014 | 0x0004 | Χαρακτηριστικά | Περιγράφει την ευθυγράμμιση. |

### Πιστοποιητικό

Ένα πιστοποιητικό είναι υποχρεωτικό για κάθε εκτελέσιμο Xbox που περιέχει πληροφορίες σχετικά με τους τίτλους:
 


- Ώρα και ημερομηνία δημιουργίας του πιστοποιητικού
- Αναγνωριστικό τίτλου
- Όνομα τίτλου
- Εναλλακτικά αναγνωριστικά τίτλων
- Επιτρεπόμενοι τύποι μέσων από τα οποία μπορεί να εκτελεστεί το εκτελέσιμο (HD, DVD, CD, κ.λπ.)
- Περιοχή παιχνιδιού
- Βαθμολογίες παιχνιδιών
- Αριθμός δίσκου
- Εκδοχή
- Ακατέργαστα δεδομένα κλειδιού LAN που χρησιμοποιούνται για τη Σύνδεση συστήματος
- Υπογραφή ακατέργαστων δεδομένων κλειδιού (χρησιμοποιούνται για την υπογραφή αποθήκευσης παιχνιδιών)
- Εναλλακτικά κλειδιά υπογραφής
- Πρωτότυπο μέγεθος του πιστοποιητικού
- Όνομα ηλεκτρονικής υπηρεσίας (δεν υπάρχει σε πρώιμα εκτελέσιμα)
- Σημαίες ασφαλείας χρόνου εκτέλεσης (δεν υπάρχουν σε πρώιμα εκτελέσιμα)
 


### Επιτρεπόμενοι τύποι μέσων
Τύποι μέσων από τους οποίους επιτρέπεται η εκτέλεση από το εκτελέσιμο αρχείο. Οι ακόλουθες τιμές είναι γνωστές:
| Τύπος μέσων | Αξία |
---------------------|------------|
| ΣΚΛΗΡΟΣ_ΔΙΣΚΟΣ | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Ενότητες
Οι ενότητες εκφράζονται από τις κεφαλίδες ενοτήτων. Οι κεφαλίδες ενότητας ξεκινούν αμέσως μετά το πιστοποιητικό και περιέχουν πληροφορίες για το πού υπάρχουν στο αρχείο οι πραγματικές ενότητες. Τουλάχιστον δύο ενότητες υπάρχουν πάντα σε ένα εκτελέσιμο Xbox:


- .κείμενο


- .data


## βιβλιογραφικές αναφορές



* [Xbe - XBox Executable](https://xboxdevwiki.net/Xbe)


