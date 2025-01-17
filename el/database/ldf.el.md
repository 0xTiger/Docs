{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "επέκταση", "αρχείο", "μορφή αρχείου", "Τύπος αρχείου βάσης δεδομένων", "Μορφή αρχείου βάσης δεδομένων", "αρχεία βάσης δεδομένων" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου LDF και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία LDF.",
  "title" :"LDF - Μορφή αρχείου κύριας βάσης δεδομένων διακομιστή SQL",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Τι είναι ένα αρχείο LDF;

Ένα αρχείο με επέκταση .ldf είναι ένα αρχείο καταγραφής που διατηρείται από τον Microsoft SQL Server που είναι ένα σχεσιακό σύστημα διαχείρισης βάσεων δεδομένων (RDBMS). Όλες οι συναλλαγές που εκτελούνται σε αρχεία κύριας βάσης δεδομένων ([MDF](/el/database/mdf/)) (όπως εισαγωγή, ενημέρωση, διαγραφή) καταγράφονται στο αρχείο LDF. Τα αρχεία LDF είναι κρίσιμα στοιχεία οποιασδήποτε βάσης δεδομένων. Σε περίπτωση αποτυχίας συστήματος, το αρχείο καταγραφής χρησιμοποιείται για την επαναφορά της βάσης δεδομένων σε συνεπή κατάσταση. Το αρχείο καταγραφής συναλλαγών μπορεί να αυξηθεί σε μέγεθος εάν οι συναλλαγές δεν δεσμευτούν πλήρως. Τα αρχεία LDF μπορούν να ανοίξουν με την εφαρμογή λογισμικού Microsoft SQL Server.

## Λειτουργίες που καταγράφονται σε Αρχείο LDF

Ένα αρχείο καταγραφής SQL καταγράφει τις ακόλουθες λειτουργίες:

* Η αρχή και το τέλος κάθε συναλλαγής.

* Κάθε τροποποίηση δεδομένων δεδομένων (εισαγωγή, ενημέρωση ή διαγραφή). Αυτό περιλαμβάνει επίσης αλλαγές από διαδικασίες αποθηκευμένες στο σύστημα ή δηλώσεις γλώσσας ορισμού δεδομένων (DDL) σε οποιονδήποτε πίνακα, συμπεριλαμβανομένων των πινάκων συστήματος.

* Κάθε έκταση και εκχώρηση σελίδων ή κατανομή.

* Δημιουργία ή απόθεση πίνακα ή ευρετηρίου.

## Μορφή αρχείου LDF

Το αρχείο LDF αποτελείται από εγγραφές συναλλαγών του SQL Server που είναι ταξινομημένες ως σειρά εγγραφών καταγραφής. Κάθε εγγραφή καταγραφής έχει έναν αριθμό ακολουθίας καταγραφής (LSN) που είναι υψηλότερος από το LSN της προηγούμενης εγγραφής. Οι συμβολοσειρές συνδέονται η μία μετά την άλλη στο αρχείο. Λόγω των σύγχρονων υπολογιστών υψηλής ταχύτητας, μπορούν να εισαχθούν εγγραφές όπου το LSN2 υπάρχει στο αρχείο καταγραφής πριν από το LSN1. Δεδομένου ότι οι λειτουργίες καταγράφονται σε μια σειρά, η αλλαγή που περιγράφεται από το LSN2 πραγματοποιήθηκε μετά την εγγραφή καταγραφής LSN1. Οι εγγραφές για μια συγκεκριμένη συναλλαγή συνδέονται προς τα πίσω χρησιμοποιώντας δείκτες που χρησιμοποιούνται και επιταχύνουν την επαναφορά της συναλλαγής.
 

## βιβλιογραφικές αναφορές

* [Αρχεία βάσης δεδομένων και ομάδες αρχείων](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Οδηγός Αρχιτεκτονικής και Διαχείρισης Καταγραφής Συναλλαγών](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server-ver15)

