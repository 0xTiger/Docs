{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε σχετικά με τη μορφή αρχείου PYC και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία PYC.",
  "title" :"PYC File Format- Python Compiled File",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## Τι είναι ένα αρχείο PYC;

Ένα αρχείο PYC είναι ένα μεταγλωττισμένο αρχείο εξόδου που δημιουργείται από πηγαίο κώδικα γραμμένο στη γλώσσα προγραμματισμού Python. Όταν το αρχείο PY εκτελείται χρησιμοποιώντας διερμηνέα Python, μετατρέπεται σε bytecode για εκτέλεση. Ταυτόχρονα, ο μεταγλωττισμένος bytecode αποθηκεύεται επίσης ως αρχείο .pyc ώστε να επαναχρησιμοποιηθεί από την προσωρινή μνήμη αργότερα, εάν υπάρχει.

## Δομή της μορφής αρχείου PYC

Τα αρχεία PYC είναι σε bytecode και οι προδιαγραφές μορφής αρχείου τους δεν είναι διαθέσιμες δημόσια. Ωστόσο, η έρευνα από ορισμένες πηγές δείχνει ότι η [δομή ενός αρχείου PYC](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) αποτελείται από:

* `Ένας μαγικός αριθμός τεσσάρων byte`r - Απλά δύο byte που αλλάζουν με κάθε αλλαγή στον κώδικα ομαδοποίησης και, στη συνέχεια, δύο byte του 0d0a.
* «Χρονική σήμανση τροποποίησης τεσσάρων byte» - Χρονική σήμανση τροποποίησης Unix του αρχείου προέλευσης που δημιούργησε το .pyc, ώστε να μπορεί να μεταγλωττιστεί εκ νέου εάν αλλάξει η πηγή.
* «Αντικείμενο κωδικοποιημένου κώδικα» - η έξοδος του marshal.dump του αντικειμένου κώδικα που είναι αποτέλεσμα της μεταγλώττισης του αρχείου προέλευσης.

## βιβλιογραφικές αναφορές

* [Η δομή των αρχείων .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)

