{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "Συσκευή eBook Rocket της Nuvo Media", "αρχείο", "επέκταση", "μορφή", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε σχετικά με τη μορφή αρχείου RB για τη συσκευή Rocket eBook της Nuvo Media και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία RB.",
  "title" :"RB - Αρχείο eBook Rocket",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Τι είναι ένα αρχείο RB;

Το αρχείο με επέκταση .rb περιέχει το περιεχόμενο του Rocket eBook. Το Rocket eBook είναι στην πραγματικότητα μια συσκευή κατασκευασμένη από τη Nuvo Media. κυκλοφόρησαν αυτήν τη συσκευή το 1998. Παρόλο που το Rocket eBook είναι ικανό να εμφανίζει εικόνες, αλλά μόνο σε ασπρόμαυρη οθόνη. Διαθέτει οθόνη 106 dpi ή 480 x 320 pixels σε οθόνη αφής 4,5 x 3 ιντσών. Το Rocket eBook συνδέεται με έναν υπολογιστή μέσω σύνδεσης σειριακής θύρας για λήψη ηλεκτρονικών βιβλίων σε μορφή αρχείου RB. Τα αρχεία RB είναι ικανά να χρησιμοποιούν DRM, αλλά αυτή η τεχνολογία δεν χρησιμοποιείται στα σύγχρονα eBook. Το αρχείο RB περιέχει συμβατικά ένα αρχείο HTML με τις εικόνες και ένα αρχείο ψευδο-OPF με όλα τα μεταδεδομένα (.info).

## Τεχνικές προδιαγραφές της μορφής αρχείου RB ##

Ένας μαγικός αριθμός (σε hex) εμφανίζεται στα πρώτα 4 byte του αρχείου: B0 0C B0 0C.

Φαίνεται ότι τα επόμενα δύο byte είναι ένας αριθμός έκδοσης, όπως "02 00", που σημαίνει κύρια έκδοση 2 και δευτερεύουσα έκδοση 0.

Τα επόμενα τέσσερα byte περιέχουν το κείμενο "NUVO", ακολουθούμενο από 4 byte των 00h.

Τα επόμενα 4 byte είναι η ημερομηνία δημιουργίας του βιβλίου, κωδικοποιημένη ως int16. Αυτό μας βάζει σε μετατόπιση 0Eh. Η παλιά έκδοση του ORocketLibrary κωδικοποιούσε την πλήρη τιμή του έτους (δηλαδή, το 1999 ήταν "CF 07", το 2000 ήταν "D0 07"). Στην πρόσφατη έκδοση, το tm_year αποθηκεύεται αυτολεξεί, δηλαδή 100 για το έτος 2000 ("64 00"). Μετά το έτος έρχεται ένα int8 που αντιπροσωπεύει τον 1 σχετικό αριθμό μήνα και ένα int8 που αντιπροσωπεύει την ημέρα του μήνα.

Τα επόμενα 6 byte είναι 00h. Για τη ρύθμιση της ώρας, αυτά ενδέχεται να είναι δεσμευμένα.

Η απόλυτη μετατόπιση του "Πίνακα περιεχομένων" περιέχεται σε ένα int32 σε μετατόπιση 18h.

Μετά από αυτό είναι ένα int32 που περιέχει το μήκος του αρχείου .rb. Αυτό χρησιμοποιείται για να καθοριστεί εάν τα αρχεία είναι πλήρη ή όχι.

Ολόκληρο αυτό το κομμάτι byte (20h έως 128h) φαίνεται να χρειάζεται μόνο από έναν τίτλο που είναι κρυπτογραφημένος. Σε μη κρυπτογραφημένους τίτλους, είναι πάντα μηδέν.

Στις περισσότερες περιπτώσεις ακολουθεί ο πίνακας περιεχομένων (σε μετατόπιση 128). Ξεκινά με μια καταμέτρηση int32 του αριθμού των καταχωρήσεων "σελίδας" (ενότητες αρχείου .rb) στο ToC. Κάθε καταχώρηση αποτελείται από ένα όνομα (με μηδενική επένδυση σε 32 byte), ακολουθούμενο από 3 int32s: το μήκος του τμήματος δεδομένων, τη θέση στο αρχείο .rb και μια σημαία για αυτήν την καταχώρηση. Από σήμερα, οι γνωστές τιμές είναι: 1 (κρυπτογραφημένη), 2 (σελίδα πληροφοριών) και 8 (ξεφουσκωμένη). Τα ονόματα είναι όλα προσαρμοσμένα, ανάλογα με τις ανάγκες, για να διασφαλιστεί ότι είναι όλα μοναδικά.

## βιβλιογραφικές αναφορές

* [E-Reader - By MobileRead](https://en.wikipedia.org/wiki/E-reader)
