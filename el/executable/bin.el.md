{
"ημερομηνία":"20-07-2023",
   "keywords":[
"ΑΠΟΘΗΚΗ",
"Αρχείο BIN",
"αρχείο",
"Επέκταση αρχείου BIN",
"επέκταση",
"αρχείο"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"ψευδές",
"toc":true,
"title":"Μορφή αρχείου BIN - Εκτελέσιμο αρχείο Unix",
   "description":"Μάθετε σχετικά με τη μορφή BIN και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία BIN.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
         "parent":"executable"
}
},
"lastmod":"2023-07-20"
}

## Τι είναι ένα αρχείο BIN;

Ένα αρχείο BIN είναι ένα εκτελέσιμο αρχείο σε λειτουργικά συστήματα που βασίζονται σε Unix όπως το Linux ή το FreeBSD. Διαθέτει ένα μεταγλωττισμένο πρόγραμμα που αποτελείται από δυαδικό κώδικα που προέρχεται από τον πηγαίο κώδικα, καθιστώντας το συμβατό με την υποκείμενη αρχιτεκτονική του συστήματος. Τα αρχεία Unix Executable BIN μπορούν να συγκριθούν με αρχεία Windows .EXE και αρχεία macOS .APP όσον αφορά τον ρόλο τους ως εκτελέσιμες μορφές.

Στον τομέα της ανάπτυξης λογισμικού για συστήματα Unix, τα αρχεία BIN χρησιμοποιούνται συνήθως από προγραμματιστές για τη συσκευασία και τη διανομή προγραμμάτων. Προσφέρουν ένα βολικό μέσο παράδοσης λογισμικού στους χρήστες, επιτρέποντας την εύκολη εγκατάσταση και εκτέλεση. Εκτός από τα αρχεία BIN, υπάρχουν και άλλοι τύποι εκτελέσιμων Unix, όπως τα [.ELF](/el/executable/elf/), .X86, [.RUN](/el/executable/run/) και .X86_64, καθένα προσαρμοσμένο σε συγκεκριμένο υλικό ή Απαιτήσεις συστήματος.

Όταν πρόκειται για την εσωτερική δομή ενός αρχείου BIN, αποτελείται από κωδικοποιημένα δεδομένα που χρησιμοποιεί το λειτουργικό σύστημα Unix για να αναγνωρίσει, να διαβάσει και να εκτελέσει το εσώκλειστο πρόγραμμα. Το σύστημα βασίζεται σε συγκεκριμένες υπογραφές αρχείων ή κεφαλίδες για να αναγνωρίσει το αρχείο BIN ως εκτελέσιμο, ακολουθούμενο από την ερμηνεία και την εκτέλεση των δυαδικών εντολών που περιέχονται μέσα.

Τα αρχεία BIN συχνά συνοδεύονται από ένα συνοδευτικό αρχείο **INSTALL.TXT**, το οποίο παρέχει λεπτομερείς οδηγίες για τη σωστή εγκατάσταση και ρύθμιση του προγράμματος. Αυτή η τεκμηρίωση διασφαλίζει ότι οι χρήστες μπορούν να πλοηγηθούν στη διαδικασία εγκατάστασης με επιτυχία και να αρχίσουν να χρησιμοποιούν το λογισμικό χωρίς επιπλοκές.

## Πώς να ανοίξετε το αρχείο BIN;

Τα αρχεία BIN δεν έχουν σχεδιαστεί για απευθείας άνοιγμα και προβολή. Ωστόσο, μπορείτε να εκτελέσετε τα προγράμματα ή να εξαγάγετε τα δεδομένα που περιέχουν. Για να αποκτήσετε πρόσβαση στα περιεχόμενα ενός αρχείου BIN, ακολουθήστε αυτά τα βήματα στη γραμμή εντολών, υποθέτοντας ότι το όνομα του αρχείου BIN είναι "sample.bin":

1. **Διασφαλίστε τα εκτελέσιμα δικαιώματα:**

Πριν εκτελέσετε το αρχείο BIN, βεβαιωθείτε ότι έχει τα απαραίτητα δικαιώματα για να εκτελεστεί ως εκτελέσιμο. Χρησιμοποιήστε την εντολή:

```
$ chmod +x sample.bin
```

Αυτή η εντολή εκχωρεί στο αρχείο εκτελέσιμα δικαιώματα.

2. **Εκτελέστε το αρχείο BIN:**

Αφού ορίσετε τα εκτελέσιμα δικαιώματα, μπορείτε να εκτελέσετε το αρχείο BIN εισάγοντας την ακόλουθη εντολή:

```
$ ./sample.bin
```

**Προειδοποίηση**

_Να είστε προσεκτικοί όταν αντιμετωπίζετε αρχεία BIN που έχετε λάβει ή αποστέλλονται μέσω email, καθώς ενδέχεται να χρησιμοποιηθούν από εγκληματίες του κυβερνοχώρου για τη διανομή κακόβουλου λογισμικού. Εκτελείτε αρχεία BIN μόνο από αξιόπιστες πηγές για να μειώσετε τον κίνδυνο κακόβουλων εκτελέσιμων επιθέσεων._

## Άλλα αρχεία BIN

Ακολουθούν άλλοι τύποι αρχείων που χρησιμοποιούν την επέκταση αρχείου **.bin**.

- [BIN - MacBinary Encoded File](/el/compression/bin/)
- [BIN - Αρχείο εικόνας δυαδικού δίσκου](/el/disc-and-media/bin/)
- [BIN - BlackBerry IT Policy File](/el/settings/bin/)
- [BIN - Sega Genesis Game ROM](/el/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/el/game/bin-pcsx/)

## βιβλιογραφικές αναφορές

* [Πώς να εκτελέσετε δυαδικά αρχεία στο Linux](https://linuzhint.com/execute-binary-files-in-linux/)

