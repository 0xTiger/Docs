{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Μορφή αρχείου Manifest Java",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου MF και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MF.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Τι είναι ένα αρχείο MF;

Ένα αρχείο με επέκταση .mf είναι ένα αρχείο Java Manifest που περιέχει πληροφορίες σχετικά με τις μεμονωμένες καταχωρήσεις αρχείων [JAR](/el/programming/jar/). Το ίδιο το αρχείο MF περιέχεται μέσα στο αρχείο JAR και παρέχει όλο τον ορισμό της επέκτασης και του πακέτου. Τα αρχεία JAR μπορούν να δημιουργηθούν για να χρησιμοποιηθούν ως εκτελέσιμο αρχείο. Σε αυτήν την περίπτωση, το αρχείο mainfest καθορίζει την κύρια κλάση της εφαρμογής που περιέχει την πρόταση **`public static void main`**. Τα αρχεία Manifest ονομάζονται MANIFEST.MF και μπορούν να ανοίξουν με οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου σε λειτουργικά συστήματα Windows, MacOS και Linux.

## Προδιαγραφές μορφής αρχείου Manifest

Οι [προδιαγραφές μορφής αρχείου Manifest](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) διατίθενται από την Oracle στον οδηγό της για τη μορφή αρχείου JAR. Ένα αρχείο Manifest αποτελείται από κύριες ενότητες που ακολουθούνται από μια λίστα ενοτήτων για μεμονωμένες εγγραφές αρχείων JAR. Κάθε ενότητα ακολουθεί ορισμένους κανόνες και περιορισμούς.

### Κύρια Ενότητες

Μια κύρια ενότητα:

* περιέχει πληροφορίες σχετικά με την ασφάλεια και τις ρυθμίσεις παραμέτρων για το αρχείο JAR
* περιέχει πληροφορίες σχετικά με την εφαρμογή ή την επέκταση στην οποία ανήκει το αρχείο JAR
* ορίζει τα κύρια χαρακτηριστικά για κάθε μεμονωμένο στοιχείο δήλωσης

**Σημείωση**: Κανένα χαρακτηριστικό σε αυτήν την ενότητα δεν μπορεί να ονομαστεί "Όνομα".

### Μεμονωμένες Ενότητες

Μια μεμονωμένη ενότητα ορίζει διάφορα χαρακτηριστικά για πακέτα ή αρχεία ενός αρχείου JAR. Κάθε ενότητα πρέπει να ξεκινά με ένα χαρακτηριστικό με το όνομα "Όνομα" του οποίου η τιμή πρέπει να είναι μια σχετική διαδρομή προς το αρχείο ή μια απόλυτη διεύθυνση URL που παραπέμπει σε δεδομένα εκτός του αρχείου.

### Προδιαγραφές Manifest

|Τα χαρακτηριστικά|Περιγραφή|
---|---|
|manifest-file|νέα γραμμή κύριας ενότητας *individual-section|
|main-section|πληροφορίες έκδοσης νέα γραμμή *main-attribute|
|version-info|Manifest-Version : version-number|
|έκδοση-αριθμός|ψηφίο+{.ψηφίο+}*|
|main-attribute|(οποιοδήποτε νόμιμο κύριο χαρακτηριστικό) νέα γραμμή|
|individual-section|Όνομα : τιμή νέα γραμμή *perentry-attribute|
|perentry-attribute|(οποιοδήποτε νόμιμο χαρακτηριστικό perentry) νέα γραμμή|
|νέα γραμμή|CR LF | LF | CR (δεν ακολουθείται από LF)|
|ψηφίο|{0-9}|

## βιβλιογραφικές αναφορές

* [Oracle - Μορφή αρχείου JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [Μορφή αρχείου JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

