{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "επέκταση", "αρχείο", "μορφή αρχείου", "Τύπος αρχείου βάσης δεδομένων", "Μορφή αρχείου βάσης δεδομένων", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου ADE και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία ADE.",
  "title" :"ADE - Πρόσβαση στο αρχείο επέκτασης έργου",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## Τι είναι ένα αρχείο ADE;

Ένα αρχείο με επέκταση .ade είναι ένα αρχείο Microsoft Access Project που περιέχει τη μεταγλωττισμένη έξοδο των πληροφοριών που περιέχονται στο αρχείο έργου ADP της Microsoft Access. Οι πληροφορίες στο αρχείο έργου της Access, εκτός της Visual Basic for Applications (VBA), είναι διαθέσιμες σε μεταγλωττισμένη μορφή σε αρχεία ADE. Τα δεδομένα αποθηκεύονται σε συμπιεσμένη μορφή σε αυτά τα αρχεία για μείωση του μεγέθους του αρχείου και βελτίωση της απόδοσης στην Access. Δεδομένου ότι το ADE είναι η μεταγλωττισμένη έξοδος του αρχείου έργου της Access, οποιοσδήποτε πηγαίος κώδικας VBA που αποτελεί μέρος του έργου, παραμένει προστατευμένος μη επιτρέποντάς του να είναι μέρος της εξόδου. Τα αρχεία ADE μπορούν να ανοίξουν στη Microsoft Access 365.

## Μορφή αρχείου ADE - Περισσότερες πληροφορίες

Τα ADE είναι μεταγλωττισμένα αρχεία Access Database που αποθηκεύονται σε δίσκο ως δυαδικά αρχεία. Η εσωτερική δομή αρχείων αυτών των αρχείων δεν είναι γνωστή.

Τα αρχεία ADE μπορούν να δημιουργήσουν προβλήματα κατά το άνοιγμα με βάση την έκδοση της Microsoft Access που έχει χρησιμοποιηθεί για τη δημιουργία αυτών των αρχείων. Οι βάσεις δεδομένων πρόσβασης που χρησιμοποιούν την έκδοση 64-bit της Microsoft Access 2010 και που έχουν μεταγλωττιστεί ως αρχεία MDE, [ACCDE](/el/database/accde/) ή ADE πρέπει να μεταγλωττιστούν εκ νέου στο Microsoft Access 2021 Service Pack 1 (SP1) για να λειτουργούν σωστά με το Access 2010 SP1. Αυτό το ζήτημα παρουσιάζεται επειδή το Access 2010 SP1 χρησιμοποιεί μια νεότερη έκδοση του αρχείου VBE7.dll (έκδοση 7.00.1619).

## βιβλιογραφικές αναφορές

* [Πρόβλημα με τα αρχεία ADE της Access](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Which Access File Formats to Use](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

