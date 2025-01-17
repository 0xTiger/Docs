{
  "date" : "2019-10-11",
  "keywords" :[ "αρχείο ico", "μορφή αρχείου ico", "τι είναι αρχείο ico", "αρχείο", "παράδειγμα ico", "επέκταση αρχείου ico", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Μορφή αρχείου εικόνας",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου ICO και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία ICO.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο ICO;

Τα αρχεία με επέκταση ICO είναι τύποι αρχείων εικόνας που χρησιμοποιούνται ως εικονίδιο για την αναπαράσταση μιας εφαρμογής στο [Microsoft Windows](https://www.microsoft.com/en-us/windows). Διατίθενται σε διαφορετικό μέγεθος, υποστήριξη χρώματος και ανάλυση για να ταιριάζουν στις απαιτήσεις της οθόνης. Μια άλλη παρόμοια μορφή αρχείου εικόνας στα Microsoft Windows είναι το [CUR](/el/image/cur/) για την αναπαράσταση του δρομέα και ορίζει ένα hotspot στην κεφαλίδα της εικόνας. Στο MacOS, οι μορφές αρχείων ICNS εξυπηρετούν τον ίδιο σκοπό με τα αρχεία ICO. Αρκετοί διαδικτυακοί ιστότοποι καθώς και εφαρμογές παρέχουν τη δυνατότητα δημιουργίας τέτοιων αρχείων και μετατροπής άλλων μορφών εικόνας όπως [BMP](/el/image/bmp/), [PNG](/el/image/png/), κ.λπ. σε μορφή αρχείου εικονιδίων. Ο επίσημος τύπος πολυμέσων Διαδικτύου που έχει καταχωριστεί στο IANA για αρχεία ICO είναι image/vnd.microsoft.icon.

## Σύντομη Ιστορία ##

Τα εικονίδια παρουσιάστηκαν με την κυκλοφορία των Microsoft Windows 1.0. Αυτά είχαν μέγεθος 32x32 και ήταν μονόχρωμα. Με την άφιξη του win32, εισήχθη υποστήριξη για εικόνες εικονιδίων σε αληθινό χρώμα με διάσταση έως και 256x256 pixel. Τα Windows XP ήταν τα πρώτα που παρείχαν υποστήριξη για εικόνες έγχρωμων εικονιδίων 32 bit, επιτρέποντας την προσθήκη στο εικονίδιο ημιδιαφανών περιοχών, όπως σκιές, κατά της παραμόρφωσης και εφέ που μοιάζουν με γυαλί. Η Microsoft συνιστά μόνο μεγέθη εικονιδίων έως 48×48 pixel για Windows XP. Τα Windows Vista πρόσθεσαν μια προβολή εικονιδίων 256×256 pixel στην Εξερεύνηση των Windows, καθώς και υποστήριξη για τη συμπιεσμένη μορφή [PNG](/el/image/png/). Με τους χρήστες που χρησιμοποιούν υψηλότερες αναλύσεις και λειτουργίες υψηλού DPI, συνιστώνται μεγαλύτερες μορφές εικονιδίων (όπως 256×256).

## Μορφή αρχείου ICO ##

Ένα μεμονωμένο αρχείο ICO αποτελείται από μία ή περισσότερες από μία μικρές εικόνες πολλαπλών μεγεθών και βάθους χρωμάτων. Η παρουσία εικόνων πολλαπλών μεγεθών είναι για κατάλληλη κλιμάκωση σε διαφορετικές αναλύσεις οθόνης. Όλες οι τιμές στα αρχεία ICO/CUR αντιπροσωπεύονται με σειρά byte [little-endian](https://en.wikipedia.org/wiki/Little-endian).

Το αρχείο ICO αποτελείται από μια κεφαλίδα εικονιδίων, έναν κατάλογο εικονιδίων,

|Πεδίο|Περιγραφή
---|---|
|Εικονίδιο Κεφαλίδα|Αποθηκεύει γενικές πληροφορίες σχετικά με το αρχείο ICO.
|Κατάλογος[1..n]|Αποθηκεύει γενικές πληροφορίες για κάθε εικόνα στο αρχείο.
|Εικονίδιο #1|Τα πραγματικά "δεδομένα" για την πρώτη εικόνα σε παλιά μορφή AND/XOR DIB ή νεότερη μορφή PNG
|...|
|Εικονίδιο #n|Δεδομένα για την τελευταία εικόνα εικονιδίου

### Κεφαλίδα ###

|Offset|Μέγεθος (σε byte)|Σκοπός
---|---|---|
|0|2|Δέσμευση. Πρέπει πάντα να είναι 0.
|2|2|Καθορίζει τον τύπο εικόνας: 1 για εικόνα εικονιδίου (.ICO), 2 για εικόνα δρομέα (.CUR). Άλλες τιμές δεν είναι έγκυρες.
|4|2|Καθορίζει τον αριθμό των εικόνων στο αρχείο.

### Ευρετήριο ###

Ο κατάλογος που περιέχεται σε ένα αρχείο ICO, που αναπαρίσταται ως δομή ICONDIR, περιέχει μια δομή ICONDIRECTORY για κάθε εικόνα στο αρχείο. Το ίδιο ακολουθείται από ένα συνεχόμενο μπλοκ όλων των δεδομένων bitmap εικόνας. Αυτό είναι όπως φαίνεται παρακάτω.

|Μετατόπιση|Μέγεθος|Περιγραφή
---|---|---|
|0 (0)|1|Το πλάτος, θα πρέπει να είναι 0 εάν είναι 256 pixel
|1 (1)|1|Ύψος, θα πρέπει να είναι 0 εάν είναι 256 pixel
|2 (2)|1|Αριθμός χρωμάτων, θα πρέπει να είναι 0 εάν υπάρχουν περισσότερα από 256 χρώματα
|3 (3)|1|Δέσμευση, θα πρέπει να είναι 0
|4 (4)|2|Τα επίπεδα χρώματος σε μορφή .ICO, θα πρέπει να είναι 0 ή 1, ή το σημείο πρόσβασης X όταν είναι σε μορφή .CUR
|6 (6)|2|Bits ανά pixel σε μορφή .ICO ή το σημείο πρόσβασης Y σε μορφή .CUR
|8 (8)|4|Μέγεθος των δεδομένων bitmap σε byte.
|12 (C)|4|Μετατόπιση στο αρχείο.

## Βιβλιογραφικές αναφορές ##

* [ICO - By Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

