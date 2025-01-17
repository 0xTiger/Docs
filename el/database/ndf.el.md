{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "επέκταση", "αρχείο", "μορφή αρχείου", "Τύπος αρχείου βάσης δεδομένων", "Μορφή αρχείου βάσης δεδομένων", "αρχεία βάσης δεδομένων" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου MDF και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία NDF.",
  "title" :"Μορφή αρχείου NDF - Κύριο αρχείο βάσης δεδομένων διακομιστή SQL",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Τι είναι ένα αρχείο NDF;

Ένα αρχείο με επέκταση .ndf είναι ένα δευτερεύον αρχείο βάσης δεδομένων που χρησιμοποιείται από τον [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) για την αποθήκευση δεδομένων χρήστη. Το NDF είναι δευτερεύον αρχείο αποθήκευσης επειδή ο διακομιστής SQL αποθηκεύει δεδομένα που καθορίζονται από τον χρήστη σε πρωτεύον αρχείο αποθήκευσης γνωστό ως [MDF](/el/database/mdf/). Το αρχείο δεδομένων NDF είναι προαιρετικό και ορίζεται από τον χρήστη για τη διαχείριση της αποθήκευσης δεδομένων σε περίπτωση που το κύριο αρχείο MDF χρησιμοποιεί όλο τον εκχωρημένο χώρο. Συνήθως αποθηκεύεται σε ξεχωριστό δίσκο και μπορεί να εξαπλωθεί σε πολλές συσκευές αποθήκευσης. Η παρουσία αρχείων MDF είναι απαραίτητη για να ανοίξετε αρχεία NDF.

## Μορφή αρχείου NDF

Η μορφή αρχείου NDF δεν διαφέρει από το [MDF](/el/database/mdf/) και χρησιμοποιεί σελίδες ως τη θεμελιώδη μονάδα αποθήκευσης δεδομένων. κάθε σελίδα ξεκινά με κεφαλίδα 96 byte που περιλαμβάνει:

* Αναγνωριστικό σελίδας
* Τύπος Δομής
* Αριθμός εγγραφών στις σελίδες
* Δείκτες για προηγούμενες και επόμενες σελίδες

### Δομή αρχείου NDF

Ένα αρχείο MDF έχει την ακόλουθη δομή δεδομένων.

* Σελίδα 0: Κεφαλίδα
* Σελίδα 1: Πρώτο PFS
* Σελίδα 2: Πρώτο GAM
* Σελίδα 3: Πρώτο SGAM
* Σελίδα 4: Αχρησιμοποίητο
* Σελίδα 5: Αχρησιμοποίητο
* Σελίδα 6: Πρώτο DCM
* Σελίδα 7: Πρώτη BCM

#### Κεφαλίδα αρχείου NDF

Ο αριθμός σελίδας 0 όλων των αρχείων περιέχει μια κεφαλίδα που αποθηκεύει μεταδεδομένα για το αρχείο.

#### Ελεύθερος χώρος σελίδας (PFS)
Το PFS προσδιορίζει την κατάσταση κατανομής και καθορίζει την ποσότητα του ελεύθερου χώρου.

* Bit 1: Υποδεικνύει εάν η σελίδα έχει εκχωρηθεί ή όχι.
* Bit 2: Υποδεικνύει εάν η σελίδα είναι από μικτή έκταση.
* Bit 3: Υποδεικνύει ότι αυτή η σελίδα είναι σελίδα IAM.
* Bit 4: Υποδεικνύει ότι αυτή η σελίδα περιέχει εγγραφές φαντασμάτων
* Bits 5 έως 7: Μια συνδυασμένη τιμή τριών bit, η οποία υποδεικνύει την πληρότητα της σελίδας ως εξής:
* 0: Η σελίδα είναι άδεια
* 1: Η σελίδα είναι 1–50% γεμάτη
* 2: Η σελίδα είναι 51–80% γεμάτη
* 3: Η σελίδα είναι 81–95% γεμάτη
* 4: Η σελίδα είναι 96–100% γεμάτη

## Σελίδα αρχείου δεδομένων

Οι σελίδες σε ένα αρχείο δεδομένων SQL Server ξεκινούν από το μηδέν (0) και αυξάνονται διαδοχικά. Κάθε αρχείο αναγνωρίζεται από έναν μοναδικό αριθμό αναγνωριστικού αρχείου. Το ζεύγος αναγνωριστικού αρχείου και αριθμού σελίδας προσδιορίζει μοναδικά μια σελίδα σε μια βάση δεδομένων. Ένα παράδειγμα που δείχνει αριθμούς σελίδων σε μια βάση δεδομένων, είναι όπως στην παρακάτω εικόνα.

{{< figure src="../ndf.png" alt="Μορφή αρχείου βάσης δεδομένων NDF" >}}

Αυτό το παράδειγμα εμφανίζει αριθμούς σελίδων σε μια βάση δεδομένων που έχει ένα κύριο αρχείο δεδομένων 4 MB και ένα δευτερεύον αρχείο δεδομένων 1 MB.

## βιβλιογραφικές αναφορές

* [Αρχεία βάσης δεδομένων και ομάδες αρχείων](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
* [Αποσύνδεση και επισύναψη βάσης δεδομένων - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [Analyzing SQL Server Data File Anatomy](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

