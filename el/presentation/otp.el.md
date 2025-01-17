{
  "date" : "2021-01-21",
  "keywords" :[ "αρχείο otp", "μορφή αρχείου otp", "τι είναι αρχείο otp", "αρχείο", "παράδειγμα otp", "επέκταση αρχείου otp", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTP - Πρότυπο παρουσίασης OpenDocument",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου OTP και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία OTP.",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2021-01-21"
}

## Τι είναι ένα αρχείο OTP;

Τα αρχεία με επέκταση .otp αντιπροσωπεύουν αρχεία προτύπων παρουσίασης που δημιουργούνται από εφαρμογές σε τυπική μορφή OASIS OpenDocument. Τα περιεχόμενα ενός τέτοιου αρχείου περιλαμβάνουν πληροφορίες παρουσίασης με τη μορφή διαφανειών με κείμενο, εικόνες, σχήματα, περιεχόμενο πολυμέσων, εφέ μετάβασης και άλλα στοιχεία διαφανειών. Αυτά τα αρχεία προτύπων χρησιμοποιούνται για τη γρήγορη δημιουργία νέων παρουσιάσεων με βάση τις πληροφορίες στυλ που είναι αποθηκευμένες στο ίδιο το πρότυπο. Τα αρχεία OTP μπορούν να δημιουργηθούν και να αποθηκευτούν με πολλές διαφορετικές εφαρμογές, όπως το Impress που συνοδεύεται από τη σουίτα OpenOffice και το Microsoft PowerPoint. Η μορφή αρχείου OTP είναι παρόμοια με τα αρχεία προτύπων του Microsoft PowerPoint [.pot](/el/presentation/pot/) και [.potx](/el/presentation/potx/).

## Μορφή αρχείου OTP

Η μορφή αρχείου OTP βασίζεται στο πρότυπο OpenDocument που υποστηρίζει την αναπαράσταση εγγράφων ως μεμονωμένο έγγραφο XML καθώς και τη συλλογή πολλών δευτερευόντων εγγράφων σε ένα μόνο συμπιεσμένο πακέτο σε μορφή [ZIP](/el/compression/zip/). Τα περιεχόμενα του αρχείου διανέμονται σε πολλαπλά αρχεία xml συσκευασμένα μαζί. Αυτά τα πολλαπλά αρχεία [XML](/el/web/xml/) περιέχουν πληροφορίες σχετικά με το στυλ, το περιεχόμενο, τις μετα-πληροφορίες και τις ρυθμίσεις του εγγράφου όπως αναφέρονται παρακάτω.

* `content.xml` – Περιεχόμενο εγγράφου και αυτόματα στυλ που χρησιμοποιούνται στο περιεχόμενο.
* `styles.xml` – Στυλ που χρησιμοποιούνται στο περιεχόμενο του εγγράφου και αυτόματα στυλ που χρησιμοποιούνται στα ίδια τα στυλ.
* `meta.xml` – Έγγραφο μετα-πληροφοριών, όπως ο συγγραφέας ή η ώρα της τελευταίας ενέργειας αποθήκευσης.
* `settings.xml` – Ρυθμίσεις για συγκεκριμένες εφαρμογές, όπως το μέγεθος του παραθύρου ή οι πληροφορίες του εκτυπωτή.

## βιβλιογραφικές αναφορές

* [OpenDocument - By Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

