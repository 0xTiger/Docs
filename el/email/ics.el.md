{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - Μορφή αρχείου iCalendar",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου ICS και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία ICS.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο ICS;

Η Προδιαγραφή Βασικού Αντικειμένου Ημερολογίου και Προγραμματισμού Διαδικτύου (iCalendar) είναι ένα πρότυπο Διαδικτύου (RFC 2445) για την ανταλλαγή και την ανάπτυξη των συμβάντων ημερολογίου και του προγραμματισμού. Η μορφή iCalendar είναι διαλειτουργική, διασφαλίζοντας έτσι την ανταλλαγή πληροφοριών ημερολογίου μεταξύ των χρηστών που έχουν διαφορετικές εφαρμογές email. Το iCalendar μορφοποιεί τα δεδομένα εισόδου ως επεκτάσεις αλληλογραφίας πολλαπλών χρήσεων Διαδικτύου (MIME) και διευκολύνει την ανταλλαγή αντικειμένων μέσω διαφορετικών πρωτοκόλλων μεταφοράς. Αυτά τα πρωτόκολλα μεταφοράς μπορεί να είναι SMTP, HTTP, ασύγχρονη επικοινωνία από σημείο σε σημείο και μεταφορά δικτύου που βασίζεται σε φυσικά μέσα.

Το iCalendar επιτρέπει στους χρήστες να μοιράζονται συμβάντα, εργασίες που εξαρτώνται από την ημερομηνία/ώρα και πληροφορίες ελεύθερου/απασχολημένου μέσω email σε άλλους χρήστες που μπορούν να απαντήσουν. Τα αρχεία iCalendar αποθηκεύονται χρησιμοποιώντας επιθήματα ".ics" ".iCalendar" ή ".ifb" με έναν τύπο MIME "text/calendar". Το iCalendar διατηρείται ως αυτόνομο χωρίς καμία εξάρτηση από το πρωτόκολλο μεταφοράς. Οι διακομιστές Ιστού (με πρωτόκολλο HTTP) μπορούν να μεταφέρουν πληροφορίες iCalendar και οι ιστοσελίδες μπορούν να περιέχουν δεδομένα iCalendar σε ενσωματωμένη μορφή χρησιμοποιώντας το iCalendar.

## Σύντομο ιστορικό της μορφής αρχείου ICS

Το 1998, η Ομάδα Εργασίας Μηχανικής Διαδικτύου (IETF) όρισε το iCalendar ως πρότυπο (RFC 2445). Το πρότυπο τεκμηριώθηκε από τους Frank Dawson (Lotus Notes Corporation) και Derik Stenerson (Microsoft). Το 2009, το πρότυπο βελτιώθηκε και πάλι από τον Bernard Desruisseaux (Oracle) ως RFC 5545. Αυτή τη φορά προστέθηκαν ορισμένες νέες δυνατότητες και ορισμένες παρωχημένες λειτουργίες καταργήθηκαν. Το 2016, το RFC 7986 κυκλοφόρησε και ενισχύθηκε στο αρχικό iCalendar RFC. Το RFC 7986 πρόσθεσε νέα χαρακτηριστικά στο κύριο αντικείμενο VCALENDAR και νέα υποστηρικτικά χαρακτηριστικά εισήχθησαν επίσης για συστήματα συνδιάσκεψης.

## Μορφή αρχείου ICS ##

Ο τύπος MIME που χρησιμοποιείται από τα δεδομένα του iCalendar είναι "κείμενο/ημερολόγιο". Το προεπιλεγμένο σύνολο χαρακτήρων για το iCalendar είναι UTF-8, ωστόσο παρέχοντας παραμέτρους στο MIME, μπορεί να χρησιμοποιηθεί διαφορετικό σύνολο χαρακτήρων. Ένα αρχείο iCalendar περιέχει ενότητες, μεταξύ αυτών των ενοτήτων "VCALENDAR", είναι η καθολική ενότητα που ενσωματώνει όλες τις άλλες ενότητες. Η ενότητα VEVENT ορίζει συμβάντα, το VTODO παραθέτει όλα τα αντικείμενα που πρέπει να κάνετε, το VJOURNAL περιέχει εγγραφές ημερολογίου και το VTIMEZONE καθορίζει πληροφορίες για τη ζώνη ώρας. επιτρέπονται πολλαπλά τμήματα παρόμοιας κατηγορίας. Για πολλά συμβάντα, πολλές ενότητες VEVENT μπορούν να υπάρχουν σε ένα αρχείο iCalendar.

### Γραμμές περιεχομένου ###

Τα αντικείμενα iCalendar είναι διατεταγμένα σε ευδιάκριτες γραμμές κειμένου "γραμμές περιεχομένου". Σε αυτήν τη μορφή αρχείου, η ακολουθία CRLF τερματίζει μια γραμμή ενώ το μήκος της γραμμής περιορίζεται σε 75 οκτάδες, εξαιρουμένης της αλλαγής γραμμής. Ένα μεγάλο στοιχείο δεδομένων μπορεί να εκτείνεται σε πολλές γραμμές.

### Διαχωριστές λίστας και πεδίων ###

Οι ιδιότητες και οι παράμετροι καθορίζουν τη λίστα τιμών που διαχωρίζονται με χαρακτήρα COMMA. Οι συμβολοσειρές quoted χρησιμοποιούνται για τιμές παραμέτρων που βασίζονται σε URI. Η λίστα των παραμέτρων μπορεί να κατασκευαστεί από την τιμή της ιδιότητας. Κάθε παράμετρος ιδιότητας σε αυτήν τη λίστα πρέπει να διαχωρίζεται με ΕΜΕΙΩΤΗΡΙΟ.

Σε μια λίστα τιμών, ένα SEMICOLON απομονώνει παραμέτρους ιδιοτήτων και ένα COMMA ξεχωριστές τιμές ιδιοτήτων. Παράδειγμα δίνεται παρακάτω:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Πολλαπλές τιμές

Ορισμένες ιδιότητες μπορεί να έχουν πολλαπλές τιμές. Η απλή δημιουργία μιας νέας γραμμής περιεχομένου με το όνομα της ιδιότητας είναι ο βασικός κανόνας για ιδιότητες πολλών τιμών. Ωστόσο, για μια μεμονωμένη τιμή με πολλές παραλλαγές γλώσσας δεν πρέπει να χρησιμοποιούνται ιδιότητες πολλών τιμών.

### Δυαδικό περιεχόμενο

Μέσα σε ένα αντικείμενο iCalendar, η τιμή ιδιότητας μπορεί να αναφέρεται σε δεδομένα δυαδικού περιεχομένου που τοποθετούνται σε μια εξωτερική οντότητα MIME χρησιμοποιώντας ένα URI. Το ενσωματωμένο δυαδικό περιεχόμενο μπορεί να χρησιμοποιηθεί σε ειδικές καταστάσεις με την παράμετρο "ENCODING", όπου η εφαρμογή πρέπει να εκφράσει ένα αντικείμενο iCalendar ως μοναδική οντότητα. Το ακόλουθο παράδειγμα εξηγεί μια ιδιότητα "ATTACH" με αναφορά URI:

ΕΠΙΣΥΝΑΨΗ: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Σετ χαρακτήρα

Αν και το προεπιλεγμένο σχήμα συνόλου χαρακτήρων για ένα iCalendar είναι UTF-8, ωστόσο δεν έχει καθοριστεί καμία παράμετρος ιδιότητας για τον καθορισμό του συνόλου χαρακτήρων μιας τιμής ιδιότητας. στις μεταφορές MIME η παράμετρος "charset" ΠΡΕΠΕΙ να χρησιμοποιείται για το υπάρχον σύνολο χαρακτήρων.

## βιβλιογραφικές αναφορές

* [Ημερολόγιο και προγραμματισμός βασικών αντικειμένων στο Διαδίκτυο](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)
