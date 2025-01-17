{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο txt", "μορφή αρχείου txt", "τι είναι αρχείο txt", "αρχείο", "παράδειγμα txt", "επέκταση αρχείου txt", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TXT - Αρχείο εγγράφου κειμένου",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου TXT και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία TXT.",
  "linktitle" : "TXT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο TXT;

Ένα αρχείο με επέκταση .TXT αντιπροσωπεύει ένα έγγραφο κειμένου που περιέχει απλό κείμενο με τη μορφή γραμμών. Οι παράγραφοι σε ένα έγγραφο κειμένου αναγνωρίζονται από τις επιστροφές μεταφοράς και χρησιμοποιούνται για την καλύτερη διευθέτηση των περιεχομένων του αρχείου. Ένα τυπικό έγγραφο κειμένου μπορεί να ανοίξει σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου ή εφαρμογή επεξεργασίας κειμένου σε διαφορετικά λειτουργικά συστήματα. Όλο το κείμενο που περιέχεται σε ένα τέτοιο αρχείο είναι σε μορφή αναγνώσιμη από τον άνθρωπο και αντιπροσωπεύεται από ακολουθία χαρακτήρων.

Τα αρχεία κειμένου μπορούν να αποθηκεύσουν μεγάλο όγκο δεδομένων, καθώς δεν υπάρχει περιορισμός στο μέγεθος των περιεχομένων. Ωστόσο, οι επεξεργαστές κειμένου που ανοίγουν τόσο μεγάλα αρχεία πρέπει να είναι έξυπνοι για τη φόρτωση και την εμφάνιση αυτών. Σχεδόν όλα τα λειτουργικά συστήματα διαθέτουν προγράμματα επεξεργασίας κειμένου που σας επιτρέπουν να δημιουργείτε και να επεξεργάζεστε αρχεία κειμένου. Για παράδειγμα, το λειτουργικό σύστημα Windows συνοδεύεται από Σημειωματάριο και Wordpad για αυτόν τον σκοπό. Ομοίως, το MacOS συνοδεύεται από TextEdit για τη δημιουργία και την επεξεργασία εγγράφων κειμένου. Υπάρχουν, ωστόσο, άλλοι δωρεάν επεξεργαστές κειμένου που είναι διαθέσιμοι επίσης μέσω του Διαδικτύου που σας παρέχουν τη δυνατότητα να εργαστείτε με Έγγραφα κειμένου όπως το Notepad++ που είναι πολύ πιο προηγμένο από άποψη λειτουργικότητας.

## Προδιαγραφές μορφής αρχείου ##

Η μορφή αρχείου κειμένου δεν έχει ειδικές προδιαγραφές μορφής αρχείου. Τα αρχεία κειμένου έχουν τύπο MIME "κείμενο/απλό" και έχουν μικρή ή καθόλου μορφοποίηση. Αυτό επιτρέπει στους επεξεργαστές κειμένου να ανοίγουν τέτοια αρχεία χωρίς άλλες απαιτήσεις. Το προεπιλεγμένο σύνολο χαρακτήρων αρχείων κειμένου είναι το ASCII που χρησιμοποιείται για τη δημιουργία και εμφάνιση των περιεχομένων αρχείων κειμένου. Οι χαρακτήρες κωδικοποιούνται χρησιμοποιώντας σετ χαρακτήρων ASCII, αλλά αυτό επιβάλλει περιορισμό χρήσης σε χαρακτήρες όπως το σύμβολο της λίρας, το σύμβολο του δολαρίου και το ευρώ που δεν μπορούν να αναπαρασταθούν χρησιμοποιώντας το σύνολο χαρακτήρων ASCII. Έτσι, τα αρχεία κειμένου μπορούν επίσης να αποθηκευτούν σε μορφή Unicode, με το UTF-8 να είναι το πιο χρησιμοποιούμενο.

### Μορφή αρχείου κειμένου των Windows ###

Τα αρχεία κειμένου στο λειτουργικό σύστημα Windows αποτελούνται από πολλές γραμμές όπου κάθε γραμμή αποτελείται από μια ακολουθία χαρακτήρων. Κάθε γραμμή υπονοούμενη από τον χρήστη ορίζεται από συνδυασμό δύο χαρακτήρων, π.χ. carriage return (CR) και Line Feed (LF). Τα αρχεία κειμένου των Windows μπορούν να είναι σε κωδικοποίηση ANSI, OEM, Unicode ή UTF-8. Η κωδικοποίηση UTF-16 βοηθά στην αποθήκευση πληροφοριών σε ένα αρχείο κειμένου που απαιτεί δύο byte για αναπαράσταση. Τέτοια αρχεία συνήθως ξεκινούν με Byte Order Mark (BOM) που επικοινωνεί την τελική κατάσταση του περιεχομένου του αρχείου. Θα πρέπει να σημειωθεί ότι άλλες εφαρμογές στο λειτουργικό σύστημα Windows μπορούν να αποθηκεύουν πληροφορίες σε μορφή αρχείου κειμένου αλλά με διαφορετικές επεκτάσεις αρχείων για να αντιπροσωπεύουν κείμενο συγκεκριμένης εφαρμογής. Για παράδειγμα, οι γλώσσες προγραμματισμού συνήθως αποθηκεύουν κώδικα σε αρχείο κειμένου αλλά με τις δικές τους επεκτάσεις.

### Μορφή αρχείου κειμένου Unix ###

Όλα αυτά τα συστήματα προσαρμόζουν ένα αρχείο κειμένου ως αρχείο του οποίου οι χαρακτήρες είναι οργανωμένοι σε μηδέν ή περισσότερες γραμμές. Κάθε γραμμή είναι μια ακολουθία μηδέν ή περισσότερων χαρακτήρων χωρίς νέα γραμμή και ενός τερματικού χαρακτήρα νέας γραμμής, συνήθως LF.

## Βιβλιογραφικές αναφορές ##

* [Μορφή αρχείου TXT](https://en.wikipedia.org/wiki/Text_file)

