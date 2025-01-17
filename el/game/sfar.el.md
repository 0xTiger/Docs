{
  "date" : "2021-10-20",
  "keywords" :[ "αρχείο sfar", "μορφή αρχείου sfar", "τι είναι ένα αρχείο sfar", "αρχείο", "παράδειγμα sfar", "Επέκταση αρχείου Mass Effect 3 DLC", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε για τη μορφή αρχείου Mass Effect 3 SFAR και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία SFAR.",
  "title" :"Αρχείο DLC SFAR - Mass Effect 3",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Τι είναι ένα αρχείο SFAR;

Ένα αρχείο με επέκταση .sfar είναι ένα αρχείο δεδομένων παιχνιδιού που χρησιμοποιείται από το Mass Effect 3 για την αποθήκευση του DLC (περιεχόμενο με δυνατότητα λήψης) σε ένα συμπιεσμένο, αποκλειστικό αρχείο. Το Mass Effect 3 είναι ένα παιχνίδι που δημιουργήθηκε από την Electronic Arts, μια κορυφαία εταιρεία ανάπτυξης παιχνιδιών. Το περιεχόμενο DLC που είναι αποθηκευμένο σε ένα αρχείο SFAR χρησιμοποιείται για την επέκταση του παιχνιδιού με πρόσθετο περιεχόμενο και δυνατότητες.

## Μορφή αρχείου SFAR - Περισσότερες πληροφορίες

Τα αρχεία SFAR αποθηκεύονται/αποθηκεύονται ως συμπιεσμένα αρχεία αρχειοθέτησης σε δυαδική μορφή αρχείου. Αυτά χρησιμοποιούν αλγόριθμους συμπίεσης LZX και LZMA για τη συμπίεση των περιεχομένων. Τα αρχεία SFAR μπορούν να ανοίξουν χρησιμοποιώντας τον Επεξεργαστή DLC που συνοδεύεται από τον ME3 Explorer. Εκτός από το SFAR, το DLC Editor μπορεί να εξαγάγει άλλα αρχεία παιχνιδιών όπως [PCC](/el/game/pcc/).

## Προδιαγραφές μορφής αρχείου SFAR

Ένα αρχείο SFAR χωρίζεται στα ακόλουθα τέσσερα κύρια κομμάτια.

### Κεφαλίδα SFAR

Το SFF Header περιέχει πληροφορίες σχετικά με τα διάφορα κομμάτια που αποτελούν το αρχείο.

### Πίνακας αρχείων SFAR

Ο πίνακας αρχείων SFAR περιέχει μια λίστα με καταχωρήσεις αρχείων όπου κάθε καταχώρηση έχει μήκος 30 byte.

### Πίνακας μεγέθους μπλοκ

Το Block-Size περιέχει πολλαπλές καταχωρήσεις, όπου κάθε καταχώρηση έχει μήκος 2 byes. Αυτή η τιμή καθορίζει το μέγεθος μπλοκ που αντιστοιχεί σε μια καταχώρηση στον πίνακα αρχείων.

### Μπλοκ

Τα μπλοκ κομμάτια σε ένα αρχείο SFAR περιέχουν τα δεδομένα μέσα στο αρχείο SFAR.

## βιβλιογραφικές αναφορές

* [Μορφή αρχείου DLC SFAR - Έρευνα](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

