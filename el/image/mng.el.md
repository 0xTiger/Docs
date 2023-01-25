{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο mng", "μορφή αρχείου mng", "τι είναι αρχείο mng", "αρχείο", "παράδειγμα mng", "επέκταση αρχείου mng", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MNG File Format - Multiple Image Network Graphics File Format",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου MNG και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MNG.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο MNG;

Ένα αρχείο με επέκταση .mng είναι μια μορφή αρχείου Multiple-image Network Graphics που είναι παρόμοια με τη μορφή εικόνας [PNG](/el/image/png/), αλλά υποστηρίζει κινούμενες εικόνες. Αναπτύχθηκε για να αποφευχθεί η υπερφόρτωση της μορφής PNG με πρόσθετες δυνατότητες κινούμενων εικόνων. Το MNG είναι επίσης παρόμοιο με τα αρχεία [GIF](/el/image/gif/), αλλά χρησιμοποιεί περισσότερη συμπίεση και υποστηρίζει πλήρη λειτουργία άλφα. Ο ανεπίσημος τύπος πολυμέσων MIME για αρχεία MNG είναι βίντεο/x-mng. Τα αρχεία MNG μπορούν να ανοίξουν σε εφαρμογές όπως το ImageMagik και το IrfanView.

## Μορφή αρχείου MNG

Η μορφή αρχείου MNG είναι παρόμοια με αυτή του PNG και χρησιμοποιεί την ίδια δομή κομματιού όπως ορίζεται στις προδιαγραφές PNG. Ένας αποκωδικοποιητής MNG πρέπει να μπορεί να αποκωδικοποιεί τις ροές δεδομένων PNG χωρίς να καθορίζει ειδικές σημαίες για οδηγίες αποκωδικοποίησης. Το MNG ομαδοποιεί πολλές εικόνες μαζί σε ένα "πλαίσιο", με ορισμένες εικόνες να χρησιμοποιούνται ως sprite για μετακίνηση από τη μια τοποθεσία στην άλλη. Ο μηχανισμός επιτρέπει την επαναχρησιμοποίηση δεδομένων εικόνας χωρίς την αναμετάδοση τους. Μπορείτε να ανατρέξετε στις [προδιαγραφές MNG](http://www.libpng.org/pub/mng/spec/) για αναφορά προγραμματιστή.

### Υπογραφή MNG

Η ροή δεδομένων MNG ξεκινά με μια υπογραφή 8 byte που περιέχει:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Αυτό είναι παρόμοιο με αυτό της υπογραφής PNG, αλλά περιέχει MNG αντί για PNG.

### Πλαίσιο MNG

Ένα πλαίσιο MNG αποτελείται από δισδιάστατη εικόνα μικρότερων εικόνων. Μπορείτε να προσπελάσετε κάθε μικρή εικόνα χρησιμοποιώντας τον συνδυασμό ευρετηρίου γραμμής και στήλης. Η μορφή είναι ικανή να αποθηκεύει τρισδιάστατα δεδομένα "voxel" που είναι διατεταγμένα σε μια σειρά από δισδιάστατα επίπεδα. Κάθε επίπεδο αντιπροσωπεύεται από μια ροή δεδομένων PNG ή Delta-PNG. Κάθε ροή δεδομένων Delta-PNG ορίζει μια εικόνα ως τις διαφορές από τη μητρική εικόνα PNG. Αυτό παρέχει έναν πολύ πιο συμπαγή τρόπο αναπαράστασης επόμενων εικόνων από τη χρήση μιας πλήρους ροής δεδομένων PNG για καθεμία.

## Βιβλιογραφικές αναφορές ##

* [MNG](http://www.libpng.org/pub/mng/)
* [Μορφή MNG v 1.0](http://www.libpng.org/pub/mng/spec/)
