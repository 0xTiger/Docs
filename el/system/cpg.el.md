{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου CPG - Αρχείο σελίδας κωδικού ESRI",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου CPG και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CPG.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## Τι είναι ένα αρχείο CPG;

Ένα αρχείο CPG είναι ένα προαιρετικό αρχείο που απαιτείται από το ESRI Shapefile που χρησιμοποιείται για τον καθορισμό της κωδικοσελίδας για τον προσδιορισμό του συνόλου χαρακτήρων που θα χρησιμοποιηθεί. Αυτά αποθηκεύονται σε μορφή αρχείου απλού κειμένου και περιέχουν πληροφορίες σχετικά με την κωδικοποίηση που εφαρμόζεται για τη δημιουργία του αρχείου σχήματος. Σε περίπτωση που ένα αρχείο CPG δεν είναι διαθέσιμο, τότε το shapefile χρησιμοποιεί την προεπιλεγμένη κωδικοποίηση του συστήματος. Ένα αρχείο CPG, εάν υπάρχει, πρέπει να έχει το ίδιο πρόθεμα με αυτό του αρχείου [SHP](/el/gis/shp/), για παράδειγμα roads.shp, roads.cpg.

Τα αρχεία CPG μπορούν να ανοίξουν με το ESRI ArcGIS Pro.

### Μορφή αρχείου CPG - Περισσότερες πληροφορίες

Κατά την προβολή ενός shapefile στο ArcCatalog ή σε οποιαδήποτε άλλη εφαρμογή ArcGIS, βλέπετε μόνο το shapefile. Αλλά στην πραγματικότητα, το shapefile χρησιμοποιεί άλλα συσχετισμένα αρχεία που διαβάζονται μαζί με το κύριο αρχείο σχήματος. Το αρχείο CPG είναι επίσης ένα από αυτά εάν υπάρχει μαζί με το κύριο αρχείο SHP.

## βιβλιογραφικές αναφορές

* [Επεκτάσεις αρχείων Shapefile
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

