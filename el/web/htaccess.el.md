{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο HTACCESS - Μορφή αρχείου HTACCESS Apache",
  "description" :"Ο οδηγός μορφής αρχείου σας για να μάθετε τι είναι ένα αρχείο HTACCESS",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο HTACCESS;

Ένα αρχείο HTACCESS είναι ένα αρχείο διαμόρφωσης Apache που παρέχει έναν μηχανισμό που επιτρέπει αλλαγές διαμόρφωσης για διαφορετικούς φακέλους/καταλόγους ενός ιστότοπου. Περιλαμβάνει οδηγίες διαμόρφωσης που ισχύουν για τον κατάλογο και τους υποκαταλόγους.

Ένα αρχείο HTACCESS εκτελεί έναν αριθμό ελέγχων, όπως ο ορισμός της σελίδας ευρετηρίου ενός ιστότοπου, η λίστα της σελίδας σφάλματος 404 (Η σελίδα δεν βρέθηκε), η εκτέλεση των ανακατευθύνσεων σελίδων 301 ή 302, ο αποκλεισμός της πρόσβασης από μια συγκεκριμένη διεύθυνση IP ή άλλους ιστότοπους. Η χρήση αρχείων .htaccess, επομένως, επιβραδύνει τη συνολική απόδοση του διακομιστή Apache [HTTP](/el/web/http/).

## Μορφή αρχείου HTACCESS

Τα αρχεία HTACCESS αποθηκεύονται σε δίσκο σε μορφή αρχείου απλού κειμένου. Αυτό σημαίνει ότι μπορείτε να ανοίξετε και να επεξεργαστείτε αυτά τα αρχεία σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου. Δεν υπάρχει όνομα πριν από το "." σε ένα αρχείο .htaccess, δείχνοντας ότι είναι ένα κρυφό αρχείο μέσα στο φάκελο.

## Συνήθεις χρήσεις ενός αρχείου HTACCESS

Πέντε συνήθεις χρήσεις ενός αρχείου HTACCESS είναι οι εξής.

### Mod_Rewrite

Ένα αρχείο HTACCESS μπορεί να χρησιμοποιηθεί για να ορίσει και να αλλάξει τον τρόπο με τον οποίο εμφανίζονται στους χρήστες οι διευθύνσεις URL και οι ιστοσελίδες σε έναν ιστότοπο.

### Αυθεντικοποίηση

Ο έλεγχος ταυτότητας μπορεί να επιτευχθεί με .htaccess δημιουργώντας ένα αρχείο κωδικού πρόσβασης που ονομάζεται .htpasswd. Αυτό επιτρέπει στους επισκέπτες του ιστότοπου να παρέχουν έναν κωδικό πρόσβασης εάν θέλουν να επισκεφτούν μια συγκεκριμένη ενότητα της ιστοσελίδας.

### Προσαρμοσμένες σελίδες σφαλμάτων

Μπορείτε να δημιουργήσετε προσαρμοσμένες σελίδες σφάλματος όπως 400 Bad Request, 401 Authorization Required, 403 Forbidden Page, 404 File not Found και 500 Internal Error με το αρχείο .htaccess. Ωστόσο, αυτά θα επιβραδύνουν την απόδοση του διακομιστή, καθώς όλοι αυτοί οι έλεγχοι θα εκτελούνται καθώς γίνεται πρόσβαση στις σελίδες.

### Τύποι MIME

Τα αρχεία Apache HTACCESS μπορούν να τροποποιηθούν ώστε να περιλαμβάνουν τύπους επεκτάσεων αλληλογραφίας πολλαπλών χρήσεων Internet (MIME). Αυτό επιτρέπει στον διακομιστή σας να υποστηρίζει την παράδοση αρχείων εφαρμογών που δεν υποστηρίζονταν από τον ιστότοπο.

### SSI

Το Server Side Includes (SSI) λειτουργεί ως εξαιρετική εξοικονόμηση χρόνου σε έναν ιστότοπο. Το SSI μπορεί να ενεργοποιηθεί εισάγοντας τον ακόλουθο κώδικα στο αρχείο .htaccess.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Παράδειγμα αρχείου Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## βιβλιογραφικές αναφορές

* [Εκμάθηση διακομιστή Apache HTTP: Αρχεία .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)
