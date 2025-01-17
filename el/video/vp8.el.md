{
  "date" : "2021-03-10",
  "keywords" :[ "VP8", "File", "Extension", "File Format", "Video Format", "TrueMotion Video", "WebRTC", "WebM"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP8 - Αρχείο βίντεο TrueMotion",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου VP8 και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία VP8.",
  "linktitle" : "VP8",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## Τι είναι ένα αρχείο VP8;

Το VP8 ανακοινώνεται από την Google ως μία από τις καλύτερες μορφές βίντεο με την καλύτερη ταχύτητα δεδομένων ποιότητας εικόνας και ταχύτητα κωδικοποίησης. Το καλύτερο πλεονέκτημα του VP8 είναι ότι αποτελεί υποκατάστατο του H.264 χωρίς δικαιώματα. Είναι μια συγκεκριμένη μορφή για την κωδικοποίηση και την αποκωδικοποίηση βίντεο υψηλής ποιότητας ως αρχείο ή bitstream. Είναι δωρεάν επειδή η Google έχει κυκλοφορήσει όλες τις πατέντες VP8 βάσει δημόσιας άδειας χωρίς δικαιώματα. Σχεδόν το 90% ή περισσότερο όλων των περιόδων σύνδεσης βίντεο WebRTC χρησιμοποιούν VP8.

## Μορφή αρχείου VP8

Το VP8 αναπτύχθηκε από την On2 Technologies το 2008 και στη συνέχεια ανήκε στην Google το 2010. Το κύριο πλεονέκτημα του κωδικοποιητή βίντεο VP8 είναι ότι είναι απαλλαγμένο από δικαιώματα με δωρεάν άδεια χρήσης. Έχει σχεδιαστεί για να παρέχει βίντεο υψηλής ποιότητας για τον ιστό και τις κινητές συσκευές. Το πρώτο κοντέινερ ήχου-βίντεο για το VP8 ήταν το WebM και αυτός ο κωδικοποιητής επιλέχθηκε ως κωδικοποιητής βίντεο WebRTC το 2011. Αυτή η μορφή αναγνωρίζεται σε πολλές βιομηχανικές εφαρμογές όπως το HTML5, η Επικοινωνία σε πραγματικό χρόνο στο Web και η αναπαραγωγή βίντεο σε διαφορετικά προγράμματα περιήγησης. Υπάρχει πλήρης ζήτηση της αγοράς για υποστήριξη αυτής της μορφής σε ανάλυση full-HD. Χρησιμοποιείται για διαφορετικούς σκοπούς, όπως τηλεδιάσκεψη, μετάδοση βίντεο και εγγραφή από κινητές συσκευές.

## Προδιαγραφές ##

### Χαρακτηριστικά του VP8
 



* Δωρεάν κωδικοποιητής βίντεο
* Η πιο προοδευτική μορφή αρχείου βίντεο
* Βελτιωμένη αντίσταση στην απώλεια πλαισίου
* Αποκωδικοποίηση βίντεο υψηλής ταχύτητας
* Εύκολο να επινοηθεί σε πλατφόρμες υλικού
* Έχει τη δυνατότητα μιας καθαρής λειτουργίας εισαγωγής, π.χ. χρήση μόνο ατομικά κωδικοποιημένων καρέ χωρίς διαδοχική πρόβλεψη, για την ενεργοποίηση της τυχαίας πρόσβασης σε εφαρμογές όπως η επεξεργασία βίντεο
* Το libvpx είναι η μόνη βιβλιοθήκη λογισμικού που είναι ικανή στην κωδικοποίηση ροών βίντεο VP8
* Το VP8 σχεδιάστηκε ρητά για να λειτουργεί κυρίως σε ένα εύρος ποιότητας

* Υπάρχει ένα ευρύ φάσμα υλικού πελάτη που είναι συνδεδεμένο στο διαδίκτυο, που εκτείνεται από φορητές συσκευές χαμηλής κατανάλωσης και εμφυτευμένες συσκευές έως τους πιο προηγμένους επιτραπέζιους υπολογιστές με πολλούς πυρήνες επεξεργαστή
* Η δειγματοληψία 420 χρωμάτων, το βάθος χρώματος 8 bit ανά κανάλι, η προοδευτική σάρωση και οι διαστάσεις εικόνας έως το μέγιστο των 16383x16383 pixel μπορούν να λειτουργήσουν απλά μέσω VP8
* Η ώθηση για ικανότητα συμπίεσης και απλότητα αποκωδικοποιητή κάτω από αυτές τις ρυθμίσεις σχεδίασης οδήγησε σε πολλά μοναδικά τεχνικά χαρακτηριστικά στο VP8 σε σύγκριση με άλλες αναγνωρισμένες μορφές συμπίεσης βίντεο
* Το VP8 χρησιμοποιεί τρία πλαίσια αναφοράς, από το πολυάριθμο σχήμα αντιστάθμισης κίνησης αναφοράς που εμφανίζεται σε άλλες μορφές
* Το VP8 δεν περιορίζεται σε ρυθμό καρέ ή ταχύτητα δεδομένων. Χρησιμοποιεί 14 bit τόσο για πλάτος όσο και για ύψος, γεγονός που κάνει την υψηλότερη ανάλυση 16384x16384 pixel

### Όρια VP8

Τα όρια του VP8 όσον αφορά την ανάλυση, τον ρυθμό δεδομένων και το ρυθμό καρέ είναι τα εξής:

* Το VP8 εξασκεί 14 bit για πλάτος και ύψος, για μέγιστη ανάλυση 16384x16384 pixel
* Το VP9 χρησιμοποιεί 16 bit για πλάτος και ύψος, για μέγιστη ανάλυση 65536x65536 pixel
* Δεν υπάρχει περιορισμός στον ρυθμό καρέ ή στον ρυθμό δεδομένων
 



 



## βιβλιογραφικές αναφορές

* [VP8 Wikipedia](https://en.wikipedia.org/wiki/VP8#:~:text=VP8%20was%20first%20released%20by,%2C%20replacing%20its%20predecessor%2C%20VP7.&text= Στις%20May%2019%2C%20at%20its,μια%20αμετάκλητη%20δωρεάν%20πατέντα%20άδεια)
* [Springer Link](https://link.springer.com/chapter/10.1007/978-81-322-1157-0_32)

