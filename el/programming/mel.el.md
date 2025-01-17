{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Maya Embedded language","αρχείο", "επέκταση", "μορφή αρχείου", "Maya 3D", "Οδηγός προγραμματισμού" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Μορφή αρχείου ενσωματωμένης γλώσσας Maya",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου MEL και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MEL.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Τι είναι ένα αρχείο MEL;

Ένα αρχείο με επέκταση .mel (Maya Embedded Language) είναι μια γλώσσα δέσμης ενεργειών που χρησιμοποιείται από την Autodesk Maya για τη δημιουργία γραφικών διεπαφών. Σας επιτρέπει να αυτοματοποιήσετε τη δημιουργία γραφικών στοιχείων χρησιμοποιώντας εκτελέσιμα σενάρια εκτός από τη γραφική διεπαφή της Maya. Το MEL σάς δίνει τη δυνατότητα να δημιουργείτε γραφικές διεπαφές χωρίς να μαθαίνετε προγραμματισμό. Αυτό επιτυγχάνεται με τη δημιουργία μακροεντολών και προσαρμοσμένων ενεργειών που επιταχύνουν τις επαναλαμβανόμενες εργασίες. Αυτές οι διαδικασίες και τα σενάρια σάς επιτρέπουν να δημιουργείτε προσαρμοσμένη μοντελοποίηση, κινούμενα σχέδια, δυναμική και απόδοση εργασιών. Το Autodesk Maya 2020 μπορεί να χρησιμοποιηθεί για το άνοιγμα και την προβολή των περιεχομένων ενός αρχείου EML.

## Μορφή αρχείου MEL - Περισσότερες πληροφορίες

Το [εγχειρίδιο αναφοράς](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) ενός προγραμματιστή είναι διαθέσιμο για προγραμματιστές στην ενότητα τεκμηρίωσης της Maya. Το MEL βασίζεται σε εντολές δέσμης ενεργειών φλοιού, παρόμοιες με το UINX, για την επίτευξη πραγμάτων. Οι εντολές που βασίζονται σε δέσμες ενεργειών το καθιστούν άσχετο με τον συμβατικό και αντικειμενοστραφή προγραμματισμό (OOP), με αποτέλεσμα να μη γίνεται χρήση δομών δεδομένων, συναρτήσεων κλήσης ή χρήσης OOP όπως σε άλλες γλώσσες.

Ορισμένα βασικά σημεία σχετικά με το MEL είναι τα ακόλουθα.

`Σχόλια` - Κάθε δήλωση στο MEL πρέπει να τελειώνει με τελεία (;), ακόμη και στο τέλος ενός μπλοκ.

`Επιστρέφοντας τιμές` - Η δήλωση μιας παράστασης που επιστρέφει μια τιμή δεν εκτυπώνει αυτόματα την τιμή σε MEL. Αντίθετα προκαλεί σφάλμα.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
"Εντολές για Δημιουργία, Επεξεργασία και Διαγραφή" - Η ίδια εντολή χρησιμοποιείται για τη δημιουργία πραγμάτων, την επεξεργασία πραγμάτων ή την αναζήτηση πληροφοριών σχετικά με υπάρχοντα πράγματα. Ωστόσο, μια σημαία ελέγχει τι κάνει η εντολή (δημιουργία, επεξεργασία ή ερώτημα).

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Επιστρεφόμενη τιμή από τη συνάρτηση` - Η σύνταξη συνάρτησης επιστρέφει αυτόματα μια τιμή. Για να λάβετε μια επιστρεφόμενη τιμή χρησιμοποιώντας τη σύνταξη εντολών, πρέπει να περικλείσετε την εντολή σε εισαγωγικά.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## βιβλιογραφικές αναφορές

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

