{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου WMV",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου WMV και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία WMV.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Τι είναι ένα αρχείο WMV;

Το Advanced Systems Format (ASF) είναι ένα ψηφιακό δοχείο πολυμέσων που έχει σχεδιαστεί κυρίως για την αποθήκευση και τη μετάδοση ροών πολυμέσων. Το Microsoft Windows Media Video (WMV) είναι η μορφή συμπιεσμένου βίντεο και το Microsoft Windows Media Audio (WMA) είναι η συμπιεσμένη μορφή ήχου μαζί με πρόσθετα μεταδεδομένα στο κοντέινερ ASF που αναπτύχθηκε από τη Microsoft. Μόλις τα αρχεία WMV ή WMA κωδικοποιηθούν με κωδικοποιητές Windows Media Video και Windows Media Audio, τότε αντιπροσωπεύονται με επέκταση .asf. Το WMV συμπιέζει μεγάλα αρχεία για καλύτερο ρυθμό μετάδοσης μέσω δικτύου διατηρώντας παράλληλα την ποιότητα του βίντεο. Το WMV έχει σχεδιαστεί ειδικά για να τρέχει σε όλες τις συσκευές Windows. Μετά την τυποποίηση από την Εταιρεία Μηχανικών Κινηματογράφου και Τηλεόρασης (SMPTE), το WMV θεωρείται πλέον μια ανοιχτή τυπική μορφή.

## Ιστορία ##

Με τη βοήθεια αποκλειστικών κωδικοποιητών της Microsoft αναπτύχθηκε νέα μορφή συμπιεσμένου βίντεο το 1999, γνωστή ως WMV7, η οποία βασίστηκε στο MPEG-4 Part 2. Προστέθηκαν βελτιώσεις σε άλλες δύο εκδόσεις, π.χ. WMV8 και 9. Η Microsoft υπέβαλε μια έκδοση 9^^th^^ του WMV στο SMPTE για τυποποίηση το 2003, το οποίο τελικά τυποποιήθηκε το 2006 ως SMPTE 421M γνωστό και ως VC-1. Η ιδέα πίσω από το WMV ήταν να αναπτυχθεί μια μορφή πολυμέσων που θα μπορούσε να υποστηριχθεί από όλο το υλικό και το λογισμικό που υποστηρίζεται από τη Microsoft. Επιπλέον, ένας άλλος σημαντικός σκοπός ήταν η μετάδοση ροών βίντεο μέσω του Διαδικτύου σε ένα βέλτιστο σενάριο. Μετά την τυποποίηση από το SMPTE, το WMV έγινε επίσης μορφή βίντεο για δίσκους Blu-ray.

## Προδιαγραφές μορφής αρχείου

### Δοχείο

Γενικά, το WMV είναι συσκευασμένο σε ένα κοντέινερ ASF, αλλά επιπλέον, το κοντέινερ Matroska ή AVI μπορεί επίσης να το υποστηρίξει με επεκτάσεις .mkv και .avi αντίστοιχα.

### Windows Media Video 9

Αν και υπάρχουν διάφοροι κωδικοποιητές ήχου και βίντεο στη σειρά Windows Media Video 9 για δημιουργία και αναπαραγωγή ψηφιακών μέσων, ο κωδικοποιητής WMV-9 είναι ο πιο πρόσφατος και καλύτερος κωδικοποιητής βίντεο, καθώς μπορεί να επιτύχει τη βέλτιστη συμπίεση από πολύ χαμηλούς ρυθμούς bit, π.χ. 160 x 120 στα 10 Kbps έως 1920 x 1080 στα 4-8 Mbps για μια ποικιλία βίντεο HD.

### Δομή του Codec

Το WMV-9 έχει εσωτερική χρωματική μορφή 8 bit 4:2:0. Όπως όλα τα άλλα δημοφιλή πρότυπα συμπίεσης βίντεο MPEG-1 και H.261, το WMV-9 χρησιμοποιεί ένα σχήμα αντιστάθμισης κίνησης και χωρικού μετασχηματισμού που βασίζεται σε μπλοκ. Γενικά, μπορούμε να πούμε ότι αυτά τα πρότυπα εκτελούν αντιστάθμιση κίνησης μπλοκ προς μπλοκ από το προηγούμενο ανακατασκευασμένο πλαίσιο με τη βοήθεια μιας δισδιάστατης ποσότητας που ονομάζεται διάνυσμα κίνησης (MV) για να σηματοδοτήσει τη χωρική μετατόπιση. Το τρέχον μπλοκ σχηματίζεται με τη βοήθεια της πρόβλεψης των τιμών από το ίδιο μέγεθος προηγούμενο ανακατασκευασμένο πλαίσιο το οποίο μετατοπίζεται από την τρέχουσα θέση από το διάνυσμα κίνησης. Τελικά, το υπολειπόμενο σφάλμα υπολογίζεται ως η διαφορά μεταξύ του προβλεπόμενου μπλοκ με αντιστάθμιση κίνησης και του πραγματικού μπλοκ. Αυτό το υπολειπόμενο σφάλμα μετασχηματίζεται χρησιμοποιώντας έναν γραμμικό μετασχηματισμό συμπίεσης ενέργειας και μετά κβαντοποιείται και κωδικοποιείται με εντροπία.

Οι κβαντισμένοι συντελεστές μετασχηματισμού αποκωδικοποιούνται με εντροπία, αποκβαντίζονται και μετασχηματίζονται αντίστροφα για να παραχθεί μια προσέγγιση του υπολειπόμενου σφάλματος στην πλευρά του αποκωδικοποιητή, το οποίο στη συνέχεια προστίθεται στην πρόβλεψη με αντιστάθμιση κίνησης για να δημιουργήσει την ανακατασκευή. Η περιγραφή υψηλού επιπέδου του κωδικοποιητή φαίνεται στην παρακάτω εικόνα.

Η υπόλοιπη ενότητα θα συζητήσει τις νέες βελτιώσεις στο WMV-9 που το διαφοροποιούν από τις υπόλοιπες λύσεις κωδικοποίησης βίντεο όπως τα πρότυπα MPEG. Το WMV-9 έχει πλαίσια (Ι), προβλεπόμενα (P) και αμφίδρομα προβλεπόμενα (Β). Τα ενδοπλαίσια είναι αυτά που κωδικοποιούνται ανεξάρτητα και δεν έχουν καμία εξάρτηση από άλλα πλαίσια. Τα προβλεπόμενα πλαίσια είναι πλαίσια που εξαρτώνται από ένα καρέ στο παρελθόν. Η αποκωδικοποίηση ενός προβλεπόμενου πλαισίου μπορεί να συμβεί μόνο αφού αποκωδικοποιηθούν όλα τα πλαίσια αναφοράς πριν από το τρέχον πλαίσιο που ξεκινούν από το πιο πρόσφατο πλαίσιο (I). Τα πλαίσια Β είναι πλαίσια που έχουν δύο αναφορές — μία στο προσωρινό παρελθόν και μία στο προσωρινό μέλλον. Τα πλαίσια Β μεταδίδονται μετά τις αναφορές τους, πράγμα που σημαίνει ότι τα πλαίσια Β αποστέλλονται εκτός σειράς για να διασφαλιστεί ότι οι αναφορές τους είναι διαθέσιμες κατά τη στιγμή της αποκωδικοποίησης. Τα πλαίσια B στο WMV-9 δεν χρησιμοποιούνται ως αναφορά για τα επόμενα πλαίσια. Αυτό τοποθετεί τα πλαίσια Β έξω από τον βρόχο αποκωδικοποίησης, επιτρέποντας τη λήψη συντομεύσεων κατά την αποκωδικοποίηση πλαισίων Β χωρίς μετατόπιση ή μακροπρόθεσμα οπτικά τεχνουργήματα. Ο παραπάνω ορισμός των πλαισίων I, P και B ισχύει τόσο για προοδευτικές όσο και για αλληλουχίες αλληλουχίας.

Η απόδοση των κωδικοποιητών βίντεο συγκρίνεται με την γραφική παράσταση ρυθμού παραμόρφωσης (RD). Είναι μια καμπύλη 2-Δ που δείχνει την παραμόρφωση που προκαλείται από τη συμπίεση σε ένα συγκεκριμένο bitrate.

Το WMV-9 έχει αντιμετωπίσει αυτό το πρόβλημα με την εισαγωγή μιας ποικιλίας τεχνικών που αναφέρονται παρακάτω:

1. Προσαρμόσιμος μετασχηματισμός μεγέθους μπλοκ

2. Σύνολο μετασχηματισμού περιορισμένης ακρίβειας

3. Αποζημίωση κίνησης

4. Κβαντοποίηση και αποκβάντιση

5. Προηγμένη κωδικοποίηση εντροπίας

6. Φιλτράρισμα βρόχου

7. Προηγμένη κωδικοποίηση πλαισίου Β

8. Πεπλεγμένη κωδικοποίηση

9. Εξομάλυνση επικάλυψης

10. Εργαλεία χαμηλής τιμής

11. Αντιστάθμιση εξασθένισης

## Βιβλιογραφικές αναφορές ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)
* [http://citeseerx.ist.psu.edu/viewdoc/download?doi#10.1.1.101.488&rep#rep1&type#pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi#10.1 .1.101.488&rep#rep1&type#pdf)
