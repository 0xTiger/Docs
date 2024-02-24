{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Μάθετε για τη μορφή αρχείου MCR και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MCR.",
  "title": "MCR - Μορφή αρχείου περιοχής Minecraft",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-elr"
}
},
  "lastmod": "2022-12-14"
}

## Τι είναι ένα αρχείο MCR;

Η μορφή αρχείου Minecraft MCR είναι μια μορφή δεδομένων που χρησιμοποιείται από το Minecraft για την αποθήκευση τμημάτων εδάφους ενός Minecraft World. Βασίζεται στη μορφή NBT (Named Binary Tag), η οποία αναπτύχθηκε από τους προγραμματιστές της δημοφιλούς μηχανής παιχνιδιών ανοιχτού κώδικα, Minecraft Forge. Ο τύπος αρχείου MCR εισήχθη στην αρχή και αργότερα αντικαταστάθηκε από το [MCA file format](/game/mca/).

## Μορφή αρχείου MCR

Η μορφή αρχείου MCR είναι δομημένη ως μια σειρά από επώνυμες δυαδικές ετικέτες, καθεμία από τις οποίες περιέχει έναν συγκεκριμένο τύπο δεδομένων. Η ετικέτα ανώτατου επιπέδου είναι η ετικέτα Επίπεδο, η οποία περιέχει όλα τα δεδομένα για ένα επίπεδο παιχνιδιού. Μέσα στην ετικέτα Level, υπάρχουν πολλές άλλες επώνυμες ετικέτες που αποθηκεύουν διαφορετικούς τύπους δεδομένων, όπως η ετικέτα Δεδομένα, η οποία αποθηκεύει πληροφορίες για τον κόσμο του παιχνιδιού και οι ετικέτες Οντότητες και TileEntities, οι οποίες αποθηκεύουν δεδομένα σχετικά με το αντικείμενα παιχνιδιού και οντότητες πλακιδίων στον κόσμο, αντίστοιχα.

## Τι υπάρχει μέσα στο MCR File Format;

Στη μορφή αρχείου Minecraft MCR, μια περιοχή είναι μια περιοχή μπλοκ 32x32 του κόσμου του παιχνιδιού. Η μορφή MCR χωρίζει τον κόσμο του παιχνιδιού σε περιοχές, προκειμένου να διαχειρίζεται τα δεδομένα πιο αποτελεσματικά και να επιτρέπει την ταχύτερη φόρτωση και αποθήκευση των επιπέδων του παιχνιδιού. Κάθε περιοχή αποθηκεύεται σε ξεχωριστό αρχείο και η μορφή αρχείου MCR χρησιμοποιεί ένα σύστημα συντεταγμένων για να προσδιορίσει τη θέση κάθε περιοχής στον κόσμο του παιχνιδιού. Οι συντεταγμένες μιας περιοχής καθορίζονται από τις συντεταγμένες μπλοκ της κάτω αριστερής γωνίας της περιοχής. Για παράδειγμα, μια περιοχή με συντεταγμένες (-1,0) θα βρίσκεται μια περιοχή στα αριστερά και μηδέν περιοχές κάτω από την αρχή του κόσμου του παιχνιδιού.

## Προδιαγραφές μορφής αρχείου MCR

Οι προδιαγραφές μορφής αρχείου MCR είναι διαθέσιμες στο κοινό. Οι προδιαγραφές για τη μορφή NBT, στην οποία βασίζεται η μορφή MCR, είναι διαθέσιμες στον ιστότοπο του Minecraft Forge. Επιπλέον, το [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) έχει επίσης λεπτομερείς πληροφορίες σχετικά με τη μορφή αρχείου MCR, συμπεριλαμβανομένης της δομής του και των διαφόρων τύπων δεδομένων που υποστηρίζει.

### Συμπιεσμένα δεδομένα σε αρχεία MCR

Η μορφή αρχείου Minecraft MCR υποστηρίζει συμπίεση. Η μορφή αρχείου MCR βασίζεται στο The [NBT format](https://minecraft.fandom.com/wiki/NBT_format) που επιτρέπει την αποθήκευση δεδομένων σε συμπιεσμένη μορφή. Αυτό βοηθά στη μείωση του μεγέθους των αρχείων MCR και στην αποτελεσματικότερη μεταφορά και αποθήκευση τους. Αυτό είναι ένα σημαντικό χαρακτηριστικό της μορφής αρχείου MCR, καθώς επιτρέπει στους παίκτες να μοιράζονται μεγάλα δεδομένα εδάφους του Minecraft World με άλλους.

## βιβλιογραφικές αναφορές

* [World Editor for Minecraft](https://www.mcedit.net/)

* [Σχετικά με το Minecraft](https://www.minecraft.net/)

* [Μορφή αρχείου περιοχής](https://minecraft.fandom.com/wiki/Region_file_format)

* [Μορφή NBT](https://minecraft.fandom.com/wiki/NBT_format)

