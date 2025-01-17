{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου CMS - Αρχείο προφίλ υπηρεσίας διαχείρισης σύνδεσης",
  "description":"Μάθετε σχετικά με το αρχείο CMS και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CMS.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Τι είναι ένα αρχείο CMS;

Ένα αρχείο CMS είναι ένα αρχείο δεδομένων που περιέχει πληροφορίες προφίλ που χρησιμοποιούνται από το Microsoft Windows Connection Manager. Επιτρέπει στους απομακρυσμένους χρήστες να συνδέονται σε ένα δίκτυο χρησιμοποιώντας αυτές τις πληροφορίες προφίλ. Οι πληροφορίες που είναι αποθηκευμένες σε ένα αρχείο CMS περιλαμβάνουν δεδομένα σχετικά με το λειτουργικό σύστημα του χρήστη και τα δικαιώματα που χρησιμοποιούνται για τη δημιουργία σύνδεσης μεταξύ ενός απομακρυσμένου χρήστη και του δικτύου. Οι διαχειριστές CMS χρησιμοποιούν το Connection Manager Administrator Kit (CMAK) για τη δημιουργία αρχείων CMS.

## Μορφή αρχείου CMS - Περισσότερες πληροφορίες

Τα αρχεία CMS δεν βρίσκονται συνήθως σε μηχανές χρηστών. Δεδομένου ότι χρησιμοποιούνται ειδικά για να επιτρέψουν σε απομακρυσμένους χρήστες σε ένα δίκτυο, θα τα βρείτε σε υπολογιστές που χρησιμοποιούνται για σύνδεση σε ένα εταιρικό δίκτυο ή σε κάποιο γραφείο για συγκεκριμένο σκοπό. Στις περισσότερες περιπτώσεις, χρησιμοποιείται για σύνδεση σε ένα οργανωτικό δίκτυο όπως το Virtual Private Network (VPN) που προορίζεται μόνο για μια εταιρεία. Ως διαχειριστής δικτύου, θα ρυθμίσετε την πρόσβαση σε ένα τέτοιο δίκτυο με το Connection Manager για να του επιτρέψετε να έχει πρόσβαση στο δίκτυο της εταιρείας από μια απομακρυσμένη τοποθεσία.

### Τι είναι το insdie CMS;

Ένα αρχείο προφίλ CMS δημιουργείται χρησιμοποιώντας το Connection Manager και συσκευάζεται με άλλα αρχεία διαμόρφωσης προτού παρασχεθεί στον απομακρυσμένο χρήστη. Αυτά τα πρόσθετα αρχεία μπορεί να περιλαμβάνουν ένα αρχείο CMP και και ένα αρχείο INF που είναι συσκευασμένα μαζί σε ένα αρχείο [EXE](/el/executable/exe/). Αυτό το πλήρες πακέτο παρέχεται στον απομακρυσμένο χρήστη για σύνδεση στο δίκτυο.

## βιβλιογραφικές αναφορές

* [Κατανόηση και ρύθμιση παραμέτρων του Windows Connection Manager](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

