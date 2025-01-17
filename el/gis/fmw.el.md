{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Αρχείο FMW - Μορφή αρχείου πάγκου εργασίας FME",
  "description":"Μάθετε για τη μορφή αρχείου FMW και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία FMW.",
  "linktitle" : "FMW",
  "menu" : {
    "docs" : {
      "identifier":"gis-fmw-el",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Τι είναι ένα αρχείο FMW;

Ένα αρχείο FMW είναι ένα αρχείο έργου που δημιουργήθηκε με το λογισμικό FME Workbench (διατίθεται ως μέρος της σουίτας επιτραπέζιων υπολογιστών FME) που χρησιμοποιείται για μετασχηματισμό χωρικών δεδομένων. Περιλαμβάνει ρυθμίσεις καθορισμένες από το χρήστη που χρησιμοποιούνται για χειρισμό χωρικών δεδομένων, όπως σύνολα δεδομένων εισόδου, ιδιότητες μετάφρασης, προβολές και ρυθμίσεις εξόδου. Οι ρυθμίσεις χειρισμού χωρικών δεδομένων αποθηκεύονται ως οπτική διάταξη και είναι εύκολο να επεξεργαστούν και να αποθηκευτούν ξανά.

Μπορείτε να ανοίξετε αρχεία FMW χρησιμοποιώντας το [Safe Software FME Desktop](https://fme.safe.com/platform/).

## Μορφή αρχείου FMW - Περισσότερες πληροφορίες

Τα αρχεία FMW αποθηκεύονται σε δίσκο ως δυαδικά αρχεία και μπορούν να διαβαστούν μόνο χρησιμοποιώντας το λογισμικό FME Desktop. Το λογισμικό μπορεί επίσης να διαβάσει δεδομένα από έναν αριθμό σχεσιακών μορφών βάσης δεδομένων και υποστηρίζει επίσης μια σειρά από μορφές δεδομένων.

### Γρήγορα στοιχεία FMW

|Γεγονός|Αξία|
---|---|
|Αναγνώστης/Συγγραφέας|Αναγνώστης|
|Επίπεδο αδειοδότησης|Βάση|
|Εξαρτήσεις|Καμία|
|Τύπος συνόλου δεδομένων|Αρχείο|
|Τύπος χαρακτηριστικού|Διορθώθηκε|
|Τυπικές επεκτάσεις αρχείων|.fmw|
|Αυτόματη υποστήριξη μετάφρασης|Ναι|
|Χαρακτηριστικά καθορισμένα από το χρήστη|Όχι|
|Υποστήριξη συστήματος συντεταγμένων|Όχι|
|Γενική υποστήριξη χρώματος|Όχι|
|Χωρικός Ευρετήριο|Αριθ.|
|Απαιτείται σχήμα|Όχι|
|Υποστήριξη συναλλαγών|Όχι|
|Γεωμετρία Τύπος Χαρακτηριστικό|Κανένα|
|Υποστήριξη κωδικοποίησης|Όχι|

### Υποστήριξη FMW Geometry

|Γεωμετρία|Υποστηρίζεται;|
---|---|
|σύνολο|όχι|
|κύκλοι|όχι|
|κυκλικό τόξο|όχι|
|ντόνατ πολύγωνο|όχι|
|ελλειπτικό τόξο|όχι|
|ελλείψεις|όχι|
|γραμμή|όχι|
|κανένα|ναι|
|σημείο|όχι|
|πολύγωνο|όχι|
|ράστερ|όχι|
|στερεό|όχι|
|επιφάνεια|όχι|
|κείμενο|όχι|
|z τιμές|όχι|


## βιβλιογραφικές αναφορές

* [Safe Software FME Desktop](https://fme.safe.com/platform/)
* [FMW Quick Facts](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_ReadersWriters/fmw/quick_facts_fmw.htm)
