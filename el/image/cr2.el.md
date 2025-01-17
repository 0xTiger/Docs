{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR2 File Format - Canon Raw 2 Image File",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου CR2 και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CR2.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Τι είναι ένα αρχείο CR2;

Ένα αρχείο CR2 (Camera RAW 2) είναι ένα αρχείο εικόνας RAW που δημιουργήθηκε από ψηφιακές φωτογραφικές μηχανές Canon. Αποθηκεύει τα αρχικά μη επεξεργασμένα δεδομένα εικόνας χωρίς απώλειες που καταγράφηκαν από την κάμερα. Η μορφή αρχείου CR2 αναπτύχθηκε από την Canon για τις ψηφιακές της φωτογραφικές μηχανές και μπορεί να καταγράψει εικόνες υψηλής ποιότητας έως και 14 bit RGB. Αυτό παράγει εικόνες υψηλής ποιότητας με αρκετό χώρο μετα-επεξεργασίας. Η μορφή εικόνας CR2 έχει χρησιμοποιηθεί από την Canon στα μοντέλα καμερών 350D, 20D και 1D. Τα αρχεία CR2 είναι αρχεία RAW και περιέχουν πρόσθετες πληροφορίες μεταδεδομένων, όπως πληροφορίες κάμερας, πληροφορίες φακού, πληροφορίες bracketing, ισορροπία λευκού και άλλες ρυθμίσεις.

## Μορφή αρχείου CR2

Τα αρχεία CR2 αποθηκεύονται στην κάρτα μνήμης της κάμερας ως δυαδικά αρχεία σε ιδιόκτητη μορφή αρχείου της Canon. Η μορφή αρχείου CR2 αντικατέστησε την αρχικά χρησιμοποιούμενη μορφή αρχείου CRW και αργότερα αντικαταστάθηκε από τη μορφή αρχείου Canon RAW 3. Η μορφή αρχείου CR2 βασίζεται στις προδιαγραφές [TIFF](/el/image/tiff/) που έχει 4 Καταλόγους αρχείων εικόνας (IFD).

|Offset |Περιεχόμενο |Σχόλιο|
---|---|---|
|0x0000 |Κεφαλίδα |περιέχει τη σειρά των byte, την έκδοση και τη μετατόπιση στην εικόνα RAW|
|υπολογισμένο |IFD#0 |αυτό το τμήμα περιέχει την ενότητα Exif, η οποία περιέχει την ενότητα Makernotes.
Πληροφορίες για την εικόνα#0|
|υπολογισμένη |εικόνα#0 |μικρή έκδοση της εικόνας (το ένα τέταρτο του μεγέθους της αρχικής), συμπιεσμένη σε Jpeg|
|υπολογισμένο |IFD#1 |Πληροφορίες για την εικόνα#1.|
|υπολογισμένη |εικόνα#1 |μικρή έκδοση της εικόνας, συμπιεσμένη σε Jpeg|
|υπολογισμένο |IFD#2 |Πληροφορίες για την εικόνα#2.|
|υπολογισμένη |εικόνα#2 |μικρή έκδοση της εικόνας, όχι συμπιεσμένη|
|στην κεφαλίδα| IFD#3| Πληροφορίες για την εικόνα#3, την εικόνα RAW πλήρους διάστασης|
|υπολογισμένη |εικόνα#3 |Δεδομένα RAW εικόνας, συμπιεσμένα χωρίς απώλειες σε Jpeg (όχι δεδομένα RGB!)|

## Πλεονέκτημα της μορφής αρχείου CR2

Η αποθήκευση εικόνων σε μορφή RAW επιτρέπει πολλή μετα-επεξεργασία στη φωτογραφία, όπως προσαρμογή στην ισορροπία λευκού. Αυτό είναι πολύ πιο δύσκολο και με μεγάλη απώλεια ποιότητας με άλλες μορφές αρχείων εικόνας όπως [JPEG](/el/image/jpeg/).

## Είναι το CR2 καλύτερο από το JPEG;

Τα αρχεία CR2 είναι ακατέργαστα αρχεία χωρίς απώλεια δεδομένων και, ως εκ τούτου, χωρίς απώλεια ποιότητας. Το JPEG από την άλλη είναι μορφή αρχείου εικόνας με απώλειες καθώς χάνει ορισμένα δεδομένα για να μειώσει το αρχείο. Έτσι, τα αρχεία CR2 είναι υψηλής ποιότητας και πιο κατάλληλα για ρετούς και βελτιώσεις.

## βιβλιογραφικές αναφορές

* [Μορφή αρχείου CR2](http://lclevy.free.fr/cr2/)

