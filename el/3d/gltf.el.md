{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "αρχείο", "επέκταση", "μορφή", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τα αρχεία GLTF και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία GLTF.",
  "title" :"GLTF - Μορφή αρχείου μετάδοσης GL",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο GLTF;

Το glTF (Μορφή μετάδοσης GL) είναι μια μορφή αρχείου 3D που αποθηκεύει πληροφορίες τρισδιάστατου μοντέλου σε μορφή JSON. Η χρήση του JSON ελαχιστοποιεί τόσο το μέγεθος των τρισδιάστατων στοιχείων όσο και την επεξεργασία χρόνου εκτέλεσης που απαιτείται για την αποσυσκευασία και τη χρήση αυτών των στοιχείων. Υιοθετήθηκε για την αποτελεσματική μετάδοση και φόρτωση τρισδιάστατων σκηνών και μοντέλων από εφαρμογές. Το glTF αναπτύχθηκε από την ομάδα εργασίας Khronos Group 3D Formats και περιγράφεται επίσης ως [JPEG](/el/image/jpeg/) του 3D από τους δημιουργούς του.

Η μορφή αρχείου GLTF ορίζει μια επεκτάσιμη, κοινή μορφή δημοσίευσης για εργαλεία και υπηρεσίες τρισδιάστατου περιεχομένου που απλοποιεί τις ροές εργασίας συγγραφής και επιτρέπει τη διαλειτουργική χρήση περιεχομένου σε ολόκληρο τον κλάδο. Η πρόθεση πίσω από τη δημιουργία της μορφής αρχείου glTF ήταν να οριστεί μια επεκτάσιμη, κοινή μορφή δημοσίευσης για εργαλεία και υπηρεσίες τρισδιάστατου περιεχομένου που θα πρέπει να εξορθολογίζει τις ροές εργασίας συγγραφής και να επιτρέπει τη διαλειτουργική χρήση περιεχομένου σε ολόκληρο τον κλάδο. Ελαχιστοποιεί την επεξεργασία χρόνου εκτέλεσης από εφαρμογές που χρησιμοποιούν WebGL και άλλα API.

## Σύντομη ιστορία του αρχείου GLTF

Οι πρώτες προδιαγραφές για τη μορφή αρχείου glTF 1.0 ανακοινώθηκαν τον Οκτώβριο του 2015. Αυτό ήταν μια σειρά προσπαθειών που ξεκίνησαν τον Μάρτιο του 2012 από την Khronos. Ο στόχος αυτών των προσπαθειών ήταν να αξιολογηθούν οι ευκαιρίες γύρω από την πρόσφυση του WebGL. Ως αποτέλεσμα, η πρώτη επίδειξη μορφής glTF, βασισμένη στη μορφή JSON παρουσιάστηκε στη συνάντηση WebGl το 2012. Η μορφή υιοθετήθηκε από πολλές εταιρείες κατά καιρούς, συμπεριλαμβανομένων των Cesium, 3D Tiles, Oculus, Microsoft, Archilogic και άλλων.

Το glTF 2.0 δημοσιεύτηκε στις 5 Ιουνίου 2017 στο συνέδριο Web3D 2017. Υπάρχει ένας μακρύς κατάλογος εταιρειών που υιοθέτησαν τη μορφή αρχείου glTF μετά από αυτό.

## Μορφή αρχείου GLTF

Οι προδιαγραφές μορφής αρχείου για το glTF 2.0 είναι διαθέσιμες [διαδικτυακά](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0) για αναφορά και θα πρέπει να συμβουλεύονται σε οποιαδήποτε εφαρμογή που σχετίζεται με την ανάγνωση/εγγραφή για υποστήριξη Μορφή αρχείου glTF.

Το glTF ορίζει τα στοιχεία ως αρχεία JSON με υποστήριξη εξωτερικών δεδομένων. Αντιπροσωπεύει τρισδιάστατα μοντέλα με τη βοήθεια:

* Πλήρης περιγραφή σκηνής που περιέχεται σε ένα αρχείο .glTF με μορφή JSON που περιλαμβάνει πληροφορίες σχετικά με την ιεραρχία κόμβων, τα υλικά, τις κάμερες, καθώς και πληροφορίες περιγραφής για πλέγματα, κινούμενα σχέδια και άλλες κατασκευές
* Δυαδικά αρχεία (.bin) που περιέχουν δεδομένα γεωμετρίας και κινούμενων εικόνων και άλλα δεδομένα που βασίζονται σε buffer
* Αρχεία εικόνας ([.jpg](/el/image/jpeg/), [.png](/el/image/png/)) για υφές

Οποιαδήποτε εξωτερικά στοιχεία, όπως εικόνες, αποθηκεύονται σε εξωτερικά αρχεία που αναφέρονται μέσω URI. Αυτά τα URI αποθηκεύονται δίπλα στο κοντέινερ GLB ή ενσωματώνονται απευθείας στο JSON χρησιμοποιώντας URI δεδομένων. Κάθε έγκυρο glTF πρέπει να προσδιορίζει την έκδοσή του.

Το glTF έχει σχεδιαστεί για να επιτυγχάνει μικρό μέγεθος αρχείου, γρήγορη φόρτωση, πλήρη αναπαράσταση 3D σκηνής και επεκτασιμότητα. Αυτοί οι μοναδικοί σχεδιαστικοί στόχοι είναι οι κύριοι λόγοι για τη δημοτικότητα της μορφής αρχείου glTF στον τομέα 3D. Ακολουθούν οι τύποι mime που υποστηρίζονται από τη μορφή αρχείου glTF για διαφορετικούς τύπους αρχείων:

* Τα αρχεία .gltf χρησιμοποιούν model/gltf+json
* Τα αρχεία .bin χρησιμοποιούν εφαρμογή/οκτάδα ροής
* Τα αρχεία υφής χρησιμοποιούν τον επίσημο τύπο εικόνας/* με βάση τη συγκεκριμένη μορφή εικόνας. Για συμβατότητα με σύγχρονα προγράμματα περιήγησης ιστού, υποστηρίζονται οι ακόλουθες μορφές εικόνας: image/jpeg, image/png.

### Κωδικοποίηση JSON

Το glTF επιβάλλει τους ακόλουθους πρόσθετους περιορισμούς στη μορφή αρχείου JSON

Για να απλοποιηθεί η υλοποίηση από την πλευρά του πελάτη, το glTF έχει πρόσθετους περιορισμούς στη μορφή και την κωδικοποίηση JSON.

1. Το JSON πρέπει να χρησιμοποιεί κωδικοποίηση UTF-8 χωρίς BOM.
1. Όλες οι συμβολοσειρές που ορίζονται σε αυτήν την προδιαγραφή (ονόματα ιδιοτήτων, αριθμοί) χρησιμοποιούν μόνο σύνολο χαρακτήρων ASCII και πρέπει να γράφονται ως απλό κείμενο, π.χ. "buffer" αντί για ""\u0062\u0075\u0066\u0066\u0065\u0072"".
1. Τα ονόματα (κλειδιά) στα αντικείμενα JSON πρέπει να είναι μοναδικά, δηλαδή δεν επιτρέπονται τα διπλά κλειδιά.

### URI

Τα buffer και οι πόροι εικόνας αναφέρονται μέσω URI. Οι ακόλουθοι δύο τύποι URI πρέπει να υποστηρίζονται από τους πελάτες.

**URI δεδομένων:** Τα URI δεδομένων είναι όπως ορίζονται από το RFC 2397 και χρησιμοποιούνται από το glTF για την ενσωμάτωση πόρων στο JSON.

**Σχετικές διαδρομές URI:** ή path-noscheme όπως ορίζεται από το RFC 3986, [Section 4.2](https://tools.ietf.org/html/rfc3986#section-4.2) — χωρίς σχήμα, αρχή ή παραμέτρους. Οι δεσμευμένοι χαρακτήρες πρέπει να είναι κωδικοποιημένοι με τοις εκατό, ανά RFC 3986, [Ενότητα 2.2](https://tools.ietf.org/html/rfc3986#section-2.2).

## Βιβλιογραφικές αναφορές ##

* [Προδιαγραφές glTF 2.0 - Khronos](https://github.com/KhronosGroup/glTF)
* [Μορφή αρχείου glTF - Από τη Wikipedia](https://en.wikipedia.org/wiki/GlTF)
