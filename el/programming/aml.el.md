
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο AML - Microsoft Assistance Markup Language File",
  "description":"Μάθετε τι είναι ένα αρχείο AML και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML - Αρχείο γλώσσας σήμανσης Microsoft Assistance

## Τι είναι ένα αρχείο AML;

Ένα αρχείο AML (Assistance Markup Language) είναι ένα αρχείο XML που δημιουργείται με τη Γλώσσα σήμανσης βοήθειας της Microsoft (MAML). Αναπτύχθηκε από τη Microsoft για να παρέχει ηλεκτρονική βοήθεια για το λειτουργικό σύστημα Microsoft Windows. Πριν από αυτό, η βοήθεια των Windows ήταν διαθέσιμη στη μεταγλωττισμένη μορφή αρχείου HTML [CHM](/el/web/chm/). Τα αρχεία AML παρέχουν ένα δομημένο έγγραφο που επιτρέπει στην εφαρμογή να δημιουργεί πηγαίο κώδικα και να υποστηρίζει σελίδες βοήθειας. Αυτό επιτρέπει τον ορισμό των εγγράφων και των συστατικών τους στοιχείων βάσει του πλαισίου τους. Τα αρχεία βοήθειας AML δημοσιεύονται στο διαδίκτυο και μπορούν να ρυθμιστούν ώστε να ενημερώνονται από τις ενημερώσεις πακέτων που είναι διαθέσιμες στο διαδίκτυο.

## Δομή αρχείου MAML

Τα αρχεία AML που δημιουργούνται με χρήση MAML αποθηκεύονται ως αρχεία [XML](/el/web/xml/) που μπορούν να χρησιμοποιηθούν για να εκφράσουν ένα ευρύ φάσμα ενεργών εννοιών. Μπορεί επίσης να παρέχει καθοδηγούμενη βοήθεια (οδηγός ενεργού περιεχομένου) που κάνει το αρχείο βοήθειας διαδραστικό για τον χρήστη με τον οδηγό βήμα προς βήμα.

Ένα αρχείο AML που δημιουργείται χρησιμοποιώντας το MAML ακολουθεί τη δομή σύνταξης του που μπορεί να χωριστεί σε τμήματα όπως:

* Εννοιολογική
* Συχνές ερωτήσεις
* Γλωσσάρι
* Διαδικασία
* Αναφορά
* Επαναχρησιμοποιήσιμο περιεχόμενο
* Εργασία
* Αντιμετώπιση προβλημάτων και
* Φροντιστήριο

## Πώς να δημιουργήσετε αρχεία MAML;

Τα αρχεία MAML μπορούν να δημιουργηθούν χρησιμοποιώντας μία από τις ακόλουθες μεθόδους:

* Χρήση Sandcastle - Χρησιμοποιεί μια σουίτα σχημάτων και εκτελέσιμων προγραμμάτων για τη δημιουργία του αρχείου βοήθειας. Αυτό το εργαλείο, ωστόσο, έχει διακοπεί.
* Χρήση DocProject - Μια προσθήκη Microsoft Visual Studio που μπορεί να εκτελεστεί από το Microsoft Visual Studio για τη δημιουργία του περιεχομένου βοήθειας.

Τα αρχεία MAML μπορούν να δημιουργηθούν χρησιμοποιώντας το Sandcastle, μια σουίτα σχημάτων .XSL και εκτελέσιμων προγραμμάτων. Μπορούν επίσης να δημιουργηθούν χρησιμοποιώντας το DocProject, ένα πρόσθετο εργαλείου συγγραφής βοήθειας του Microsoft Visual Studio.

## βιβλιογραφικές αναφορές

* [Δημιουργήστε βοήθεια που βασίζεται σε XML χρησιμοποιώντας το PlatyPS](https://learn.microsoft.com/en-us/powershell/utility-modules/platyps/create-help-using-platyps?view=ps-modules)
* [Microsoft Assistance Markup Language](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML - Αρχείο γλώσσας Arc Macro

## Τι είναι ένα αρχείο ARC Macro AML;

Ένα αρχείο AML (ARC Macro Language) είναι ένα αρχείο δέσμης ενεργειών που δημιουργείται με την εφαρμογή ArcInfo Workstation GIS. Είναι γραμμένο στη γλώσσα ARC Macro, η οποία είναι μια ιδιόκτητη αλγοριθμική γλώσσα υψηλού επιπέδου για τη δημιουργία εφαρμογών GIS στο ArcInfo. Το AML σχεδιάστηκε από την ESRI το 1986 και εξυπηρετούσε το σκοπό της δημιουργίας εφαρμογών από το σύστημα της γραμμής εντολών ARCINFO GIS. Ως αρχείο δέσμης ενεργειών, τα αρχεία AML μπορούν να περιέχουν εντολές σεναρίου για την εκτέλεση ορισμένων εργασιών, όπως η δημιουργία στοιχείων διεπαφής χρήστη και ο χειρισμός δεδομένων χάρτη.

## Μορφή αρχείου AML - Περισσότερες πληροφορίες

Η AML, ως αρχεία δέσμης ενεργειών, αποθηκεύει τις πληροφορίες σε δίσκο ως αρχεία απλού κειμένου. Ακολουθεί τη σύνταξη AML που βασίστηκε στη γλώσσα κελύφους CPL του λειτουργικού συστήματος PRIMOS. Η γλώσσα AML έχει αντικατασταθεί από το πλαίσιο γεωεπεξεργασίας της ESRI που αποτελεί μέρος της σουίτας ArcGIS και χρησιμοποιεί ArcObjects για να παρέχει υποστήριξη προγραμματισμού μέσω VBA ή Python.

## βιβλιογραφικές αναφορές

* [ARC Macro Language](https://en.wikipedia.org/wiki/ARC_Macro_Language)
* [Χρήση AML με Εργαλεία Σεναρίων](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

