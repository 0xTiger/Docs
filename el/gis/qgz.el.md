{
  "date" : "2021-03-18",
  "keywords" :[ "αρχείο qgz", "μορφή αρχείου qgz", "τι είναι αρχείο qgz", "αρχείο", "παράδειγμα qgz", "επέκταση αρχείου qgz", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Quantum GIS Compresed Project",
  "description":"Μάθετε για τη μορφή αρχείου QGZ που είναι απλώς ένα συμπιεσμένο QGS και API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία QGZ.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Τι είναι ένα αρχείο QGZ;

Η μορφή αρχείου **QGZ** είναι ένα συμπιεσμένο αρχείο που περιέχει ένα αρχείο [QGS](https://docs.fileformat.com/gis/qgs/) και ένα αρχείο QGD. Ενώ, το αρχείο QGD είναι η βάση δεδομένων sqlite του έργου qgis που αποτελείται από βοηθητικά δεδομένα για το έργο. Εάν δεν υπάρχουν βοηθητικά δεδομένα, το αρχείο QGD θα παραμείνει κενό.

## Λεπτομέρειες σχετικά με τη μορφή αρχείου QGZ

Το QGZ εισήχθη ως μια νέα παραλλαγή της μορφής αρχείου έργου **QGIS 3**. Αυτή η μορφή είναι ένα συμπιεσμένο κοντέινερ για το αρχείο QGS xml. Εάν οι χρήστες επιλέξουν το QGD που είναι προαιρετική μορφή, σε αυτήν την περίπτωση το κοντέινερ είναι επωφελές για την αποθήκευση της βοηθητικής βάσης δεδομένων αποθήκευσης.

Στην κλασική λειτουργία, η βοηθητική βάση δεδομένων αποθηκεύεται ως αρχείο με επέκταση .qgd κατά μήκος του αρχείου xml. Κατά την επιλογή του συμπιεσμένου κοντέινερ, το αρχείο .qgd περιλαμβάνεται στο .qgz, απλώς διευκολύνει τους χρήστες χωρίς κανένα πρόβλημα, οι χρήστες δεν μπορούν να το διαγράψουν ή να ξεχάσουν να το αντιγράψουν κατά την κοινή χρήση αρχείων έργου!


## βιβλιογραφικές αναφορές

* [QGZ – Μια νέα προεπιλεγμένη μορφή αρχείου έργου για το QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Μορφές αρχείων QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)
