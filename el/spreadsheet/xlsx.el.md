{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "αρχείο", "επέκταση", "μορφή αρχείου", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε τι είναι ένα αρχείο XLSX και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία XLSX.",
  "title" :"Μορφή αρχείου XLSX - Τι είναι ένα αρχείο XLSX;",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Τι είναι ένα αρχείο XLSX;

Το **XLSX** είναι μια πολύ γνωστή μορφή για έγγραφα του Microsoft Excel που εισήχθη από τη Microsoft με την κυκλοφορία του Microsoft Office 2007. Βασίζεται στη δομή που οργανώθηκε σύμφωνα με τις Συμβάσεις Ανοιχτής Συσκευασίας όπως περιγράφεται στο [Μέρος 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) του προτύπου OOXML ECMA-376, η νέα μορφή είναι ένα πακέτο zip που περιέχει έναν αριθμό αρχείων XML. Η υποκείμενη δομή και τα αρχεία μπορούν να εξεταστούν απλά αποσυμπιέζοντας το αρχείο .xlsx.

## Σύντομο ιστορικό της μορφής αρχείου XLSX

Η μορφή αρχείου XLSX εισήχθη το 2007 και χρησιμοποιεί το πρότυπο Open XML που προσαρμόστηκε από τη Microsoft το 2000. Πριν από το XLSX, η κοινή μορφή αρχείου που χρησιμοποιήθηκε ήταν [XLS](/el/spreadsheet/xls/) που ήταν καθαρή μορφή δυαδικού αρχείου. Ο νέος τύπος αρχείου έχει πρόσθετα πλεονεκτήματα μικρών μεγεθών αρχείων, λιγότερων αλλαγών στη φθορά και καλής μορφοποίησης αναπαράστασης εικόνων. Ήταν στις αρχές του 2000 όταν η Microsoft αποφάσισε να προχωρήσει στην αλλαγή για να καλύψει το πρότυπο για το **Office Open XML**. Μέχρι το 2007, αυτή η νέα μορφή αρχείου έγινε μέρος του Office 2007 και εφαρμόζεται και στις νέες εκδόσεις του Microsoft Office.

## Προδιαγραφές μορφής αρχείου XLSX

Οι επίσημες [προδιαγραφές μορφής αρχείου XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) είναι διαθέσιμες στο διαδίκτυο από τη Microsoft. Για να δείτε τι βρίσκεται μέσα στο αρχείο XLSX, απλώς μετονομάστε το σε αρχείο [ZIP](/el/compression/zip/) αλλάζοντας την επέκτασή του και, στη συνέχεια, εξαγάγετε το για να προβάλετε τα συστατικά αρχεία αυτού του βιβλίου εργασίας του Excel. Ένα κενό βιβλίο εργασίας, όταν εξάγεται στα αρχεία του, έχει τα ακόλουθα συστατικά αρχεία και φακέλους.

### [Τύποι_περιεχομένου].xml ###

Αυτό είναι το μόνο αρχείο που βρίσκεται στο βασικό επίπεδο κατά την εξαγωγή του zip. Παραθέτει τους τύπους περιεχομένου για εξαρτήματα εντός του πακέτου. Όλες οι αναφορές στα αρχεία XML που περιλαμβάνονται στο πακέτο αναφέρονται σε αυτό το αρχείο XML.

### \_rels (Φάκελος) ###

Αυτός είναι ο φάκελος Relationships που περιέχει ένα μόνο αρχείο XML που αποθηκεύει τις σχέσεις σε επίπεδο πακέτου. Οι σύνδεσμοι προς τα βασικά μέρη των αρχείων Xlsx περιέχονται σε αυτό το αρχείο ως URI. Αυτά τα URI προσδιορίζουν τον τύπο σχέσης κάθε βασικού τμήματος με το πακέτο. Αυτό περιλαμβάνει τη σχέση με το κύριο έγγραφο γραφείου που βρίσκεται ως xl/workbook.xml και άλλα μέρη εντός του docProps ως βασικές και εκτεταμένες ιδιότητες.

### docProps ###

Αυτός ο φάκελος περιέχει τις συνολικές ιδιότητες του εγγράφου. Αυτές περιλαμβάνουν ένα σύνολο βασικών ιδιοτήτων, ένα σύνολο εκτεταμένων ιδιοτήτων ή ιδιοτήτων για συγκεκριμένες εφαρμογές και μια προεπισκόπηση μικρογραφίας του εγγράφου. Ένα κενό βιβλίο εργασίας έχει δύο αρχεία σε αυτόν τον φάκελο, συγκεκριμένα το app.xml και το core.xml. Το core.xml περιέχει πληροφορίες όπως ο συγγραφέας, η ημερομηνία δημιουργίας και αποθήκευσης και τροποποίησης. Το App.xml περιέχει πληροφορίες σχετικά με το περιεχόμενο του αρχείου.

### xl (Φάκελος) ###

Αυτός είναι ο κύριος φάκελος που περιέχει όλες τις λεπτομέρειες σχετικά με τα περιεχόμενα του βιβλίου εργασίας. Από προεπιλογή, έχει τους ακόλουθους φακέλους:

* \_rels
* θέμα
* φύλλα εργασίας

και τα ακόλουθα αρχεία xml:

* styles.xml
* βιβλίο εργασίας.xml

## Παράδειγμα μορφής XLSX ##


Για κάθε φύλλο εργασίας του Excel που περιέχεται σε ένα βιβλίο εργασίας, υπάρχει ένα αρχείο XML. Μπορείτε να βρείτε αυτά τα αρχεία XML στον φάκελο xl/φύλλα εργασίας. Όλες οι πληροφορίες που περιέχονται σε ένα φύλλο εργασίας είναι οργανωμένες σε διαφορετικές ενότητες του αρχείου XML. Ας εξετάσουμε ένα δείγμα φύλλου εργασίας από ένα βιβλίο εργασίας που φαίνεται στην παρακάτω εικόνα.

{{< figure src="../XLSX file format.png" alt="Μορφή αρχείου XLSX" >}}

Όπως φαίνεται, αυτό το φύλλο εργασίας περιέχει περιεχόμενα στα κελιά A1 έως B2 και μια εικόνα. Επιπλέον, το κελί G13 είναι αυτήν τη στιγμή το ενεργό κελί στο φύλλο εργασίας. Τώρα, ας εξετάσουμε το αρχείο xl/worksheets/sheet1.xml για να δούμε πώς αναπαρίστανται αυτές οι πληροφορίες στο αρχείο XML. Τα περιεχόμενα αυτού του αρχείου XML είναι όπως φαίνεται παρακάτω.

{{< figure src="../XLSX File Format Details.png" alt="Μορφή αρχείου XPS" >}}

1. Η καρτέλα έχει χρώμα θέματος που εφαρμόζεται σε αυτήν. Αναφέρεται στο αρχείο XML με ετικέτα<tabColor> ακολουθώντας το αναγνωριστικό θέματος.
1. Η τιμή tabSelected ορίζεται σε 1 που δείχνει ότι αυτό είναι το επιλεγμένο φύλλο
1. Όπως φαίνεται στην πρώτη εικόνα παραπάνω, το κελί G13 στο φύλλο εργασίας είναι ενεργό κελί το οποίο αναφέρεται επίσης στο αρχείο XML.
1. Η καρτέλα sheetData αντιπροσωπεύει τα δεδομένα που περιέχονται στο φύλλο εργασίας. Ωστόσο, μπορείτε να δείτε ότι τα αρχικά περιεχόμενα του φύλλου εργασίας δεν βρίσκονται πουθενά σε αυτήν την ενότητα. Αυτό συμβαίνει επειδή το κείμενο αναφέρεται έμμεσα από το φύλλο XML "sharedStrings". Αυτή η σύνδεση διασφαλίζει ότι κάθε κείμενο αποθηκεύεται μόνο μία φορά και μπορεί να γίνει ξανά αναφορά για εξοικονόμηση χώρου.
1. Η εικόνα, όπως φαίνεται, αναφέρεται με το αναγνωριστικό αναφοράς "rId2"

## Συνεισφέρουν

Πρέπει να μοιραστείτε κάτι σχετικά με τις μορφές αρχείων XLSX ή υπολογιστικών φύλλων; Μπορείτε να δημοσιεύσετε τα ευρήματά σας στην ενότητα [Ειδήσεις μορφής αρχείου υπολογιστικού φύλλου](https://news.fileformat.com/t/Spreadsheet).

## βιβλιογραφικές αναφορές

* [[MS-XLSX] - Μορφή αρχείου XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)
