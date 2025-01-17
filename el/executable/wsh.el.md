{
  "date" : "2021-08-27",
  "keywords" :[ "αρχείο wsh", "μορφή αρχείου wsh", "τι είναι αρχείο wsh", "αρχείο", "παράδειγμα wsh", "επέκταση αρχείου wsh", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε σχετικά με τη μορφή αρχείου WSH και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία WSH.",
  "title" :"WSH - Αρχείο δέσμης ενεργειών των Windows",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## Τι είναι ένα αρχείο WSH;
Ένα αρχείο με επέκταση .wsh περιέχει ιδιότητες και παραμέτρους για ένα συγκεκριμένο σενάριο γλώσσας προγραμματισμού όπως VB ή VBS κ.λπ. Η πραγματική ανάγκη του WSH είναι να τα χρησιμοποιήσει για την προσαρμογή της εκτέλεσης ορισμένων σεναρίων. Το WScript ή το CScript απαιτείται για εκτέλεση και τα δύο περιλαμβάνονται στο λειτουργικό σύστημα Windows. Τα αρχεία WSH αρχικά παρέχονταν στα Windows 95 στους δίσκους εγκατάστασης ως προαιρετικό με δυνατότητα διαμόρφωσης και εγκατάστασης για τον Πίνακα Ελέγχου και, στη συνέχεια, ως προεπιλεγμένο στοιχείο των Windows 98.

## Μορφή αρχείου WSH
Το WSH (Windows Script Host) μπορεί να χρησιμοποιηθεί για διάφορους σκοπούς, όπως διαχείριση, σενάρια σύνδεσης και γενική αυτοματοποίηση. Το WSH δημιουργεί ένα περιβάλλον για εκτέλεση σεναρίων. καλεί τον κατάλληλο μηχανισμό δέσμης ενεργειών και εκχωρεί ένα σύνολο υπηρεσιών και αντικειμένων για να εργαστεί το σενάριο. Αυτά τα σενάρια μπορούν να εκτελεστούν σε λειτουργία GUI, από ένα αντικείμενο COM ή τη λειτουργία γραμμής εντολών, παρέχοντας ευελιξία στον χρήστη τόσο για διαδραστικά όσο και για μη διαδραστικά σενάρια.

### Παραδείγματα
Εδώ είναι ένα πολύ απλό παράδειγμα που δείχνει κάποια VBScript που χρησιμοποιεί το ριζικό αντικείμενο WSH COM "WScript" για να εμφανίσει ένα μήνυμα με ένα κουμπί "OK". Όταν θα ξεκινήσει αυτό το σενάριο, θα κληθεί η μηχανή CScript ή WScript και θα δημιουργηθεί το περιβάλλον χρόνου εκτέλεσης.

```
WScript.Echo "Hello world"
WScript.Quit
```


## βιβλιογραφικές αναφορές

* [Windows Script Host - by Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)



