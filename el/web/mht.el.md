{
  "date" : "2019-10-11",
  "keywords" :[ "mht", "αρχείο mht", "μορφή αρχείου mht", "τύπος αρχείου mht", "αρχείο", "τύπος", "τι είναι ένα αρχείο mht" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHT - Μορφή αρχείου MIME HTML",
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου MHT και τα API για τη δημιουργία και το άνοιγμα αρχείων MHT.",
  "linktitle" : "MHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Τι είναι ένα αρχείο MHT;

Ένα αρχείο με επέκταση .mht είναι μια μορφή αρχείου αρχειοθέτησης με δυνατότητα MIME που περιέχει διαφορετικούς τύπους δεδομένων σε ένα μόνο αρχείο. Μπορεί να αποθηκεύσει δεδομένα όπως κείμενο, εικόνες, στυλ σελίδας με τη μορφή αρχείων [CSS](/el/web/css/), JavaScript και άλλους πόρους ως ενσωματωμένους πόρους σε αυτό. Τα αρχεία MHT, με μήνυμα τύπου MIME/rfc822, ενσωματώνουν όλα τα περιεχόμενα ενός αρχείου HTML ως ένα ενιαίο αρχείο αρχειοθέτησης για αποθήκευση κατά την αρχειοθέτηση σε συσκευές αποθήκευσης. Οι εφαρμογές λογισμικού όπως το Microsoft Word σάς επιτρέπουν να μετατρέψετε τα έγγραφά σας WORD σε MHT με εξαγωγή ως αρχείο MHT. Τα αρχεία MHT μπορούν να ανοίξουν χρησιμοποιώντας δημοφιλή προγράμματα περιήγησης όπως το Microsoft Internet Explore και το Google Chrome.

## Μορφή αρχείου MHT

Όπως το [MHTML](/el/web/mhtml/), το MHT είναι επίσης μια ενθυλάκωση MIME συγκεντρωτικών εγγράφων HTML. Τα περιεχόμενα εγγράφων μέσα σε ένα έγγραφο MHT, όπως ενσωματωμένες εικόνες, φύλλα στυλ, μικροεφαρμογές κ.λπ. κωδικοποιούνται με MIME όπου συνδέονται με έναν πόρο ρίζας μέσω URI. Τα προγράμματα-πελάτες ηλεκτρονικού ταχυδρομείου, όπως το Microsoft Outlook, αποθηκεύουν μηνύματα ηλεκτρονικού ταχυδρομείου (συνήθως [EML](/el/email/eml/)) σε μορφή αρχείου MHT. Οι πλήρεις προδιαγραφές της μορφής αρχείου MHT είναι διαθέσιμες στο [RFC 822](https://tools.ietf.org/html/rfc822) και μπορούν να αναφερθούν για ανάπτυξη εφαρμογών λογισμικού που μπορούν να επεξεργαστούν αρχεία MHT.

## Διαφορά μεταξύ MHT και MHTML

Κατά την αποθήκευση μιας ηλεκτρονικής σελίδας, ο χρήστης καλείται να καθορίσει το είδος της μορφής αρχείου εντός της οποίας πρέπει να αποθηκευτεί η ηλεκτρονική σελίδα στο εγγενές σύστημα. Συνήθως, ο χρήστης μπερδεύεται μεταξύ της γλώσσας σήμανσης και των μορφών αρχείων MHTML. Παρατηρούν ότι είναι ενοχλητικό να βλέπουν ότι η μορφή αρχείου είναι πιο υγιής μεταξύ αυτών.

Όταν ένας χρήστης αποφασίσει να αποφύγει τη σπατάλη της ηλεκτρονικής σελίδας ως γλώσσα σήμανσης, τότε σχηματίζεται ένας φάκελος, ο οποίος περιέχει πολλά αρχεία για διάφορα περιεχόμενα της σελίδας, δηλαδή εντελώς διαφορετική μονάδα περιοχής αρχείων που δημιουργήθηκε για κείμενο, γραφικά, μικροεφαρμογές κ.λπ. Από την αντίθετη πλευρά, η αποθήκευση η ηλεκτρονική σελίδα ως MHTML δημιουργεί ένα αρχείο για την πλήρη ηλεκτρονική σελίδα. Όλα τα στοιχεία της σελίδας μαζί με γραφικά, συνδέσμους και εναλλακτικές μονάδες περιοχής αρχείων ενσωματωμένα σε ένα αρχείο.

Φυσικά, είναι εύκολο να χειριστείτε αρχεία MHT ή MHTML επειδή το αρχείο, το οποίο μπορεί να προστατεύεται και να κοινοποιείται απλώς μέσω του ηλεκτρονικού ταχυδρομείου. Ωστόσο, η μονάδα της περιοχής αρχείων γλώσσας σήμανσης κάτω από την πιθανότητα απώλειας πληροφοριών καθώς η απώλεια ή η διαγραφή έστω και ενός αρχείου θα μπορούσε να καταστήσει τον πλήρη φάκελο της γλώσσας σήμανσης άχρηστο για τον χρήστη.

## βιβλιογραφικές αναφορές

* [MHTML - Wikipedia](https://en.wikipedia.org/wiki/MHTML)
* [MHT RFC](https://tools.ietf.org/html/rfc822)
