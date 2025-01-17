{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου MK3D",
  "keywords" :[ "mk3d", "matroska video", "mkv format", "stereoscopic 3d", "StereoMode", "video", "file", "format" ],
  "description":"Μάθετε σχετικά με τη μορφή αρχείου MK3D για στερεοσκοπικά τρισδιάστατα βίντεο που δημιουργούνται από τη Matroska και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία MK3D.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## Τι είναι ένα αρχείο MK3D; ##

Τα αρχεία MK3D ανήκουν στην οικογένεια μορφών βίντεο Matroska. Αυτά τα αρχεία είναι στην πραγματικότητα **στερεοσκοπικά 3d** βίντεο που δημιουργήθηκαν με τη μορφή Matroska 3D. Το κοντέινερ αρχείου MKV χρησιμοποιεί την τιμή ενός πεδίου StereoMode για να καθορίσει τον τύπο στερεοσκοπικού υλικού τρισδιάστατου βίντεο. Μια τιμή StereoMode είναι επίσης διαθέσιμη για την εμφάνιση των παλιών στερεοφωνικών 3D βίντεο διαχωρίζοντας τα κυανό και τα κόκκινα χρώματα (AnaGlyph)

## Τεχνικές λεπτομέρειες ##
Τα τρισδιάστατα βίντεο μπορούν να συμπιεστούν με τους εξής δύο τρόπους:

- Ξεχωριστή διαδρομή για κάθε μάτι.
- Συνδυάστε κάθε παρακολούθηση ματιών σε ένα μόνο κομμάτι.

Το κοντέινερ αρχείου MKV υποστηρίζει και τα δύο.

Για τα βίντεο ενός κομματιού που είναι ευκολότερα με το υλικό 3D μέσα σε αυτά, πρέπει να ορίσετε το πεδίο **StereoMode** που αποφασίζει είτε τα επίπεδα συναρμολογούνται στο μονοφωνικό ή στο αριστερό δεξιό συνδυασμένο κομμάτι. Μπορείτε να χρησιμοποιήσετε μία από τις ακόλουθες τιμές πεδίου StereoMode:

|Αξία | Περιγραφή |
|---|---|
|0| μονο|
|1| δίπλα δίπλα (το αριστερό μάτι είναι πρώτο)|
|2| πάνω-κάτω (πρώτο το δεξί μάτι)|
|3| πάνω-κάτω (το αριστερό μάτι είναι πρώτο)|
|4| ταμπλό (πρώτο το δεξί)|
|5| ταμπλό (αριστερά είναι το πρώτο)|
|6| γραμμή παρεμβαλλόμενη (η δεξιά είναι η πρώτη)|
|7| γραμμή παρεμβαλλόμενη (αριστερά είναι η πρώτη)|
|8| στήλη παρεμβαλλόμενη (η δεξιά είναι η πρώτη)|
|9| στήλη παρεμβαλλόμενη (αριστερά είναι η πρώτη)|
|10| ανάγλυφο (κυανό/κόκκινο)|
|11| δίπλα δίπλα (πρώτο το δεξί μάτι)|
|12| ανάγλυφο (πράσινο/ματζέντα)|
|13| και τα δύο μάτια δεμένα σε ένα Block (το αριστερό μάτι είναι πρώτο) (διαδοχική λειτουργία πεδίου)|
|14| και τα δύο μάτια δεμένα σε ένα Block (το δεξί μάτι είναι πρώτο) (διαδοχική λειτουργία πεδίου)|

Για τα πολλαπλά κομμάτια, το κοντέινερ MKV πρέπει να αποφασίσει τη λειτουργικότητα κάθε διαδρομής ξεχωριστά. Το **TrackOperation** με **TrackCombinePlanes** χρησιμοποιούνται για την εκτέλεση της εργασίας.


## Βιβλιογραφικές αναφορές ##

- [Σημειώσεις προδιαγραφών Matroska](https://www.matroska.org/technical/notes.html)
- [MKV File Container Support for Stereo 3D Video and the MK3D Files](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

