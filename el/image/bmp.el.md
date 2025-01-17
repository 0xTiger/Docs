{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο bmp", "μορφή αρχείου bmp", "τι είναι αρχείο bmp", "αρχείο", "παράδειγμα bmp", "επέκταση αρχείου bmp", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Μορφή αρχείου εικόνας",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου BMP και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία BMP.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# Τι είναι ένα αρχείο BMP; #

Τα αρχεία με επέκταση .BMP αντιπροσωπεύουν αρχεία εικόνας Bitmap που χρησιμοποιούνται για την αποθήκευση ψηφιακών εικόνων bitmap. Αυτές οι εικόνες είναι ανεξάρτητες από τον προσαρμογέα γραφικών και ονομάζονται επίσης μορφή αρχείου bitmap ανεξάρτητα από τη συσκευή (DIB). Αυτή η ανεξαρτησία εξυπηρετεί το σκοπό του ανοίγματος του αρχείου σε πολλές πλατφόρμες όπως τα Microsoft Windows και Mac. Η μορφή αρχείου BMP μπορεί να αποθηκεύσει δεδομένα ως δισδιάστατες ψηφιακές εικόνες τόσο σε μονόχρωμη όσο και σε έγχρωμη μορφή με διάφορα βάθη χρωμάτων.

## Προδιαγραφές μορφής αρχείου BMP ##

Τα Bitmaps ανεξάρτητα από τη συσκευή λειτουργούν ως βοήθημα για την ανταλλαγή bitmaps μεταξύ συσκευών και εφαρμογών. Λόγω της συνεχούς εξέλιξης αυτής της μορφής αρχείου, οι πληροφορίες που περιέχονται στις κεφαλίδες μπορεί να διαφέρουν ανάλογα με την έκδοση του Bitmap. Ένα μεμονωμένο αρχείο bitmap αποτελείται από δομές σταθερού καθώς και μεταβλητού μεγέθους σε μια συγκεκριμένη ακολουθία.

Οι δομές σε ένα αρχείο Bitmap ταξινομούνται με την ακόλουθη σειρά:


|Δομή|Προαιρετικό|Μέγεθος|Σκοπός
---|---|---|---|
|Κεφαλίδα αρχείου|Όχι|14|Για αποθήκευση γενικών πληροφοριών σχετικά με το αρχείο εικόνας bitmap
|DIB Header|No|Fixed-Size|Για να αποθηκεύσετε λεπτομερείς πληροφορίες σχετικά με την εικόνα bitmap και να ορίσετε τη μορφή pixel
|Μάσκες Extra Bit|Ναι|12 ή 16 byte|Για να ορίσετε τη μορφή pixel
|Παλέτα χρωμάτων|Ημι-προαιρετικό|Μεταβλητό μέγεθος|Για τον καθορισμό των χρωμάτων που χρησιμοποιούνται από τα δεδομένα εικόνας bitmap
|Κενό1|Ναι|Μεταβλητό μέγεθος|Στοίχιση δομής
|Pixel Array|No|Variable-size|Η μορφή pixel ορίζεται από την κεφαλίδα DIB ή τις μάσκες Extra bit.
|Κενό2|Ναι|Μεταβλητό μέγεθος|Στοίχιση δομής
|ICC Προφίλ χρώματος|Ναι|Μεταβλητό μέγεθος|Για να ορίσετε το προφίλ χρώματος για τη διαχείριση χρωμάτων

Όταν μια εικόνα bitmap φορτώνεται στη μνήμη, μετατρέπεται σε δομή DIB, που χρησιμοποιείται από τα Windows μέσω του GDI API. Η κεφαλίδα αρχείου δεν αποτελεί μέρος αυτής της δομής δεδομένων. Το χρώμα μπορεί επίσης να αποτελείται από καταχωρήσεις 16-bit που αποτελούν ευρετήρια στην παλέτα που αναφέρεται αυτή τη στιγμή αντί για σαφείς ορισμούς χρωμάτων RGB. Ας ρίξουμε μια ματιά σε μερικά από αυτά λεπτομερώς, ειδικά τις κεφαλίδες.

### Κεφαλίδα αρχείου Bitmap ###

Μια κεφαλίδα αρχείου Bitmap είναι παρόμοια με άλλες κεφαλίδες αρχείων που χρησιμοποιούνται για την αναγνώριση του αρχείου. Δεδομένου ότι υπάρχουν διαφορετικές παραλλαγές στη μορφή αρχείου BMP, τα πρώτα 2 byte της μορφής αρχείου BMP είναι ο χαρακτήρας "B" και μετά ο χαρακτήρας "M" στην κωδικοποίηση ASCII. Όλες οι ακέραιες τιμές αποθηκεύονται σε μικρή μορφή.

|Offset hex|Offset dec|Μέγεθος|Σκοπός
---|---|---|---|
|00|0|2 byte|Το πεδίο κεφαλίδας που χρησιμοποιείται για την αναγνώριση του αρχείου BMP και DIB είναι 0x42 0x4D σε δεκαεξαδικό, ίδιο με το BM στο ASCII. Μπορεί να ακολουθεί πιθανές τιμές.* **BM** – Windows 3.1x, 95, NT, ... κ.λπ. * **BA** – OS/2 struct array bitmap * **CI** – OS/2 struct έγχρωμο εικονίδιο * **CP** – δείκτης χρώματος OS/2 const * **IC** – Εικονίδιο δομής OS/2 * **PT** – δείκτης OS/2
|02|2|4 byte|Το μέγεθος του αρχείου BMP σε byte
|06|6|2 byte|Δέσμευση; Η πραγματική τιμή εξαρτάται από την εφαρμογή που δημιουργεί την εικόνα
|08|8|2 byte|Δέσμευση; Η πραγματική τιμή εξαρτάται από την εφαρμογή που δημιουργεί την εικόνα
|0A|10|4 byte|Η μετατόπιση, δηλαδή η διεύθυνση έναρξης, του byte όπου μπορούν να βρεθούν τα δεδομένα εικόνας bitmap (πίνακας εικονοστοιχείων).

#### Κεφαλίδα DIB (κεφαλίδα πληροφοριών bitmap) ####

Οι λεπτομερείς πληροφορίες σχετικά με την εικόνα αντιπροσωπεύονται από αυτήν την κεφαλίδα. Με βάση αυτές τις πληροφορίες, θα καθοριστεί η εφαρμογή που θα χρησιμοποιηθεί για την εμφάνιση της εικόνας στην οθόνη. Όλες αυτές οι κεφαλίδες περιέχουν ένα πεδίο DWORD (32-bit), που καθορίζει το μέγεθός τους, έτσι ώστε μια εφαρμογή να μπορεί εύκολα να προσδιορίσει την κεφαλίδα που χρησιμοποιείται στην εικόνα. Αυτό οφείλεται βασικά στο γεγονός ότι η μορφή DIB υποβλήθηκε σε αρκετές επεκτάσεις. Ακολουθεί η κεφαλίδα DIB με τα πεδία που αναφέρονται.

#### Παλέτα χρωμάτων ####

Μια χρωματική παλέτα BMP είναι μια σειρά από δομές που καθορίζουν τις τιμές έντασης RGB κάθε χρώματος στη χρωματική παλέτα μιας συσκευής οθόνης. Κάθε pixel στα δεδομένα bitmap αποθηκεύει μια μεμονωμένη τιμή που χρησιμοποιείται ως ευρετήριο στην παλέτα χρωμάτων. Οι πληροφορίες χρώματος που είναι αποθηκευμένες στο στοιχείο σε αυτό το ευρετήριο καθορίζουν το χρώμα αυτού του εικονοστοιχείου. Η διαθεσιμότητα χρώματος σε ένα αρχείο bitmap ποικίλλει ως εξής:

* Ένα, 4 και 8-bit - αναμένεται να περιέχει πάντα μια χρωματική παλέτα
* Δεκαέξι, 24 και 32-bit - ποτέ δεν περιέχουν χρωματικές παλέτες
* Αρχεία BMP δεκαέξι και 32 bit - περιέχουν τιμές μάσκας πεδίων bit στη θέση της παλέτας χρωμάτων

#### Αποθήκευση pixel ####

Τα εικονοστοιχεία bitmap αποθηκεύονται ως bit συσκευασμένα σε σειρές όπου το μέγεθος κάθε σειράς στρογγυλοποιείται σε ένα πολλαπλάσιο των 4 byte (ένα DWORD 32 bit) μέσω padding. Η συνολική ποσότητα byte που απαιτείται για την αποθήκευση των εικονοστοιχείων μιας εικόνας δεν μπορεί να υπολογιστεί άμεσα μετρώντας απλώς τα bit. Δεδομένου ότι υπάρχει συμπλήρωση, απαιτείται το αποτέλεσμα της στρογγυλοποίησης του μεγέθους κάθε σειράς σε πολλαπλάσιο των 4 byte. Τα byte συμπλήρωσης (όχι απαραίτητα 0) πρέπει να προσαρτηθούν στο τέλος των σειρών για να εμφανιστεί το μήκος των σειρών σε πολλαπλάσιο των τεσσάρων byte. Όταν ο πίνακας εικονοστοιχείων φορτώνεται στη μνήμη, κάθε σειρά πρέπει να ξεκινά από μια διεύθυνση μνήμης που είναι πολλαπλάσιο του 4.

Η εικόνα περιγράφεται στην πραγματικότητα από την αναπαράσταση DWORD 32-bit της διάταξης pixel. Συνήθως τα εικονοστοιχεία αποθηκεύονται «από κάτω προς τα πάνω», ξεκινώντας από την κάτω αριστερή γωνία, πηγαίνοντας από αριστερά προς τα δεξιά και στη συνέχεια σειρά με σειρά από κάτω προς τα πάνω της εικόνας. Οι μορφές pixel και οι επιπτώσεις τους αναφέρονται παρακάτω:

* Η μορφή 1 bit ανά pixel (1 bpp) υποστηρίζει 2 διαφορετικά χρώματα, (για παράδειγμα: μαύρο και άσπρο).
* Η μορφή 2 bit ανά pixel (2bpp) υποστηρίζει 4 διαφορετικά χρώματα και αποθηκεύει 4 pixel ανά 1 byte, με το πιο αριστερό pixel να βρίσκεται στα δύο πιο σημαντικά bit. Κάθε τιμή pixel είναι ένας δείκτης 2 bit σε έναν πίνακα έως και 4 χρωμάτων.
* Η μορφή 4 bit ανά pixel (4bpp) υποστηρίζει 16 διαφορετικά χρώματα και αποθηκεύει 2 pixel ανά 1 byte, με το πιο αριστερό εικονοστοιχείο να βρίσκεται στο πιο σημαντικό nibble. Κάθε τιμή pixel είναι ένας δείκτης 4 bit σε έναν πίνακα έως και 16 χρωμάτων.
* Η μορφή 8 bit ανά pixel (8bpp) υποστηρίζει 256 διαφορετικά χρώματα και αποθηκεύει 1 pixel ανά 1 byte. Κάθε byte είναι ένα ευρετήριο σε έναν πίνακα έως και 256 χρωμάτων.
* Η μορφή 16 bit ανά pixel (16bpp) υποστηρίζει 65536 διαφορετικά χρώματα και αποθηκεύει 1 pixel ανά WORD 2 byte. Κάθε WORD μπορεί να ορίσει τα δείγματα άλφα, κόκκινο, πράσινο και μπλε του pixel.
* Η μορφή 24-bit pixel (24bpp) υποστηρίζει 16.777.216 διαφορετικά χρώματα και αποθηκεύει τιμή 1 pixel ανά 3 byte. Κάθε τιμή pixel ορίζει τα κόκκινα, πράσινα και μπλε δείγματα του pixel (8.8.8.0.0 σε συμβολισμό RGBAX). Συγκεκριμένα, με τη σειρά: μπλε, πράσινο και κόκκινο (8 bit ανά δείγμα).
* Η μορφή 32 bit ανά pixel (32 bpp) υποστηρίζει 4.294.967.296 διαφορετικά χρώματα και αποθηκεύει 1 pixel ανά DWORD 4 byte. Κάθε DWORD μπορεί να ορίσει τα δείγματα άλφα, κόκκινο, πράσινο και μπλε του pixel.

## Βιβλιογραφικές αναφορές ##

* [Μορφή Windows MetaFile](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [Μορφή αρχείου BMP](https://en.wikipedia.org/wiki/BMP_file_format)

