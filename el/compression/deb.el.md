{
  "date" : "2021-04-08",
  "keywords" :[ "αρχείο deb", "μορφή αρχείου deb", "τι είναι αρχείο deb", "αρχείο", "παράδειγμα deb", "επέκταση αρχείου deb", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Bzip Compressed Tar Archive",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου DEB και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία DEB.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Τι είναι ένα αρχείο DEB;

Ένα αρχείο με επέκταση .deb είναι μια μορφή αρχείου δυαδικού πακέτου Debian διαθέσιμη για διανομή πακέτων λογισμικού σε Linux OS. Αποτελείται από δύο [TAR](/el/compression/tar/) αρχεία αρχειοθέτησης. Το DPKG παρέχει τον μηχανισμό ανάγνωσης και εγκατάστασης των πακέτων DEB. Τα πακέτα DEB μπορούν να εγκατασταθούν χρησιμοποιώντας τη διεπαφή διαχείρισης λογισμικού πακέτων APT. Τα αρχεία DEB έχουν Τύπο πολυμέσων Internet ως «application/vnd.debian.binary-package».

## Μορφή αρχείου DEB

Ένα αρχείο DEB αποτελείται από δύο αρχεία αρχειοθέτησης [TAR](/el/compression/tar/). Ένα αρχείο περιέχει τις πληροφορίες ελέγχου και ένα άλλο περιέχει τα δεδομένα που μπορούν να εγκατασταθούν.

### Οργάνωση πακέτων

Το αρχείο DEB είναι ένα αρχείο αρχειοθέτησης **ar** που έχει μια μαγική τιμή `!<arch> `. Από το Debian 0.93, ο μηχανισμός αρχειοθέτησης των αρχείων DEB περιέχει τρία αρχεία με συγκεκριμένη σειρά.

1. `Debian Binary` - Προορίζεται να έχει μια σειρά από γραμμές, χωρισμένες με νέες γραμμές. Προς το παρόν, υπάρχει μόνο μία γραμμή που περιγράφει τον αριθμό έκδοσης. Ο τρέχων αριθμός έκδοσης είναι 2.0.
1. «Αρχείο ελέγχου» - Περιέχει ένα αρχείο control.tar που έχει σενάρια συντήρησης και μετα-πληροφορίες σχετικά με το πακέτο, όπως όνομα πακέτου, έκδοση, εξαρτήσεις και συντηρητής.
1. «Αρχείο δεδομένων» - Είναι ένα αρχείο tar που ονομάζεται data.tar και περιέχει τα πραγματικά αρχεία πολυμέσων με δυνατότητα εγκατάστασης. Το αρχείο μπορεί να συμπιεστεί με gz, bz2, lzma ή xz και η επέκταση αρχείου του αρχείου δεδομένων αλλάζει ανάλογα.

### Αρχείο ελέγχου

Το αρχείο ελέγχου μπορεί να περιλαμβάνει περιεχόμενα ως εξής.

* `control` - Περιέχει μια σύντομη περιγραφή του πακέτου καθώς και άλλες πληροφορίες, όπως οι εξαρτήσεις του.
* `md5sums` - Περιέχει άθροισμα ελέγχου MD5 όλων των αρχείων του πακέτου για τον εντοπισμό κατεστραμμένων ή ελλιπών αρχείων.
* `conffiles` - Εμφανίζει τα αρχεία του πακέτου που πρέπει να αντιμετωπίζονται ως αρχεία διαμόρφωσης. Τα αρχεία διαμόρφωσης δεν αντικαθίστανται κατά τη διάρκεια μιας ενημέρωσης, εκτός εάν ορίζεται.
* `preinst`, postinst, prerm και postrm - Προαιρετικά σενάρια που εκτελούνται πριν ή μετά την εγκατάσταση ή την αφαίρεση του πακέτου
* Το "config" είναι ένα προαιρετικό σενάριο που υποστηρίζει τον μηχανισμό διαμόρφωσης debconf.
* `shlibs` - Είναι μια λίστα με κοινόχρηστες εξαρτήσεις βιβλιοθήκης.

## βιβλιογραφικές αναφορές

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Μορφή δυαδικού πακέτου Debian](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)
