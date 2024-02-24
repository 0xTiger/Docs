{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Αρχείο EAZ - Τι είναι ένα αρχείο EAZ και πώς να το ανοίξετε;",
  "description":"Μάθετε για τη μορφή αρχείου EAZ και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία EAZ.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-elz"
}
},
  "lastmod" : "2023-12-23"
}

## Τι είναι ένα αρχείο EAZ;

Το αρχείο EAZ είναι ένα πρόσθετο αρχείο που χρησιμοποιείται από τον ArcGIS Explorer, μια δωρεάν εφαρμογή που αναπτύχθηκε από την ESRI για εξερεύνηση, οπτικοποίηση και κοινή χρήση χαρτών. Περιέχει ένα συμπιεσμένο αρχείο αρχείων που περιλαμβάνει ένα [XML file](/web/xml/), μεταγλωττισμένο κώδικα και υποστηρικτικά αρχεία που είναι απαραίτητα για το πρόσθετο. Αυτά τα αρχεία χρησιμοποιούνται για την επέκταση της βασικής λειτουργικότητας του λογισμικού ενσωματώνοντας νέα κουμπιά, παράθυρα με δυνατότητα σύνδεσης και άλλες επεκτάσεις.

## Μορφή αρχείου EAZ - Περισσότερες πληροφορίες

Τα αρχεία EAZ δημιουργούνται μέσω της χρήσης του ArcGIS Explorer SDK, ενός κιτ ανάπτυξης που έχει σχεδιαστεί για τη δημιουργία προσαρμοσμένων λειτουργιών εντός του ArcGIS Explorer. Αυτά τα αρχεία χρησιμοποιούν συμπίεση [ZIP](/compression/zip/) για να πακετάρουν αποτελεσματικά τα περιεχόμενά τους. Στον πυρήνα του αρχείου, το αρχείο **Addins.xml** βρίσκεται στον ριζικό κατάλογο, χρησιμεύοντας ως ζωτικό στοιχείο που περιγράφει και περιγράφει λεπτομερώς τις διάφορες προσαρμογές που είναι ενσωματωμένες στο αρχείο EAZ.

Το αρχείο Addins.xml ουσιαστικά λειτουργεί ως οδικός χάρτης, προσφέροντας πληροφορίες για τις συγκεκριμένες βελτιώσεις, τροποποιήσεις και επεκτάσεις που εισάγει το αρχείο EAZ στον ArcGIS Explorer. Μέσω αυτής της ολοκληρωμένης δομής, οι προγραμματιστές μπορούν να ενσωματώσουν και να ενσωματώσουν απρόσκοπτα νέες δυνατότητες, κουμπιά και παράθυρα με δυνατότητα σύνδεσης, βελτιώνοντας τη συνολική λειτουργικότητα και την εμπειρία χρήστη της εφαρμογής ArcGIS Explorer.

## βιβλιογραφικές αναφορές

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)