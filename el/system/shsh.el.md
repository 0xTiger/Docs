{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο SHSH - Μορφή αρχείου SHSH Blob για iPhone/iPod Touch",
  "description":"Μάθετε για το τι είναι ένα αρχείο SHSH.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Τι είναι ένα αρχείο SHSH;

Ένα αρχείο SHSH, γνωστό και ως Signature HaSH, είναι μια ψηφιακή υπογραφή που χρησιμοποιείται από την Apple για τον έλεγχο ταυτότητας και την επαλήθευση ενημερώσεων υλικολογισμικού για συσκευές iOS όπως iPhone, iPad και iPod.

## Διαφορά μεταξύ μορφών αρχείων SHSH και SHSH2

Όπως ένα αρχείο SHSH2, το αρχείο SHSH περιέχει ένα μοναδικό αναγνωριστικό για τη συσκευή που ονομάζεται "ECID" (Αποκλειστικό Αναγνωριστικό Chip), καθώς και πληροφορίες σχετικά με την έκδοση υλικολογισμικού που είναι εγκατεστημένη στη συσκευή. Ωστόσο, τα αρχεία SHSH χρησιμοποιήθηκαν σε παλαιότερες εκδόσεις του iOS (πριν από το iOS 10) και έκτοτε έχουν αντικατασταθεί από αρχεία SHSH2.

## Μορφή αρχείου SHSH - Περισσότερες πληροφορίες

Τα αρχεία SHSH αποθηκεύονται σε δίσκο σε δυαδική μορφή αρχείου. Οι λεπτομέρειες της εσωτερικής δομής του αρχείου αυτής της μορφής αρχείου δεν είναι διαθέσιμες δημόσια.

Τα αρχεία SHSH είναι σημαντικά για χρήστες που θέλουν να υποβαθμίσουν το υλικολογισμικό της συσκευής τους σε προηγούμενη έκδοση που δεν είναι πλέον υπογεγραμμένη από την Apple. Αποθηκεύοντας τα αρχεία SHSH για μια συγκεκριμένη έκδοση υλικολογισμικού όταν εξακολουθεί να υπογράφεται από την Apple, οι χρήστες μπορούν αργότερα να τα χρησιμοποιήσουν για να παρακάμψουν την επαλήθευση υπογραφής της Apple και να εγκαταστήσουν αυτήν την έκδοση υλικολογισμικού στη συσκευή τους. Αυτή η διαδικασία είναι επίσης γνωστή ως «jailbreaking».

## βιβλιογραφικές αναφορές

* [SHSH Blob - By Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [Εξοικονόμηση TSS](https://tsssaver.1conan.com/v2/)

