{
"ημερομηνία": "2023-06-08",
  "keywords": [
"αρχείο vmx",
"τι είναι ένα αρχείο vmx",
"παράδειγμα αρχείου vmx",
"πώς να ανοίξω αρχείο vmx",
"τι περιέχει το αρχείο vmx",
"ποια είναι η μορφή του αρχείου vmx",
"αρχείο",
"επέκταση αρχείου vmx",
"επέκταση"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "VMX File Format - VMware Virtual Machine Configuration File",
  "description":"Μάθετε σχετικά με τη μορφή VMX και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία VMX.",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
      "parent": "settings"
}
},
"lastmod": "2023-06-08"
}

## Τι είναι ένα αρχείο VMX;

Ένα αρχείο VMX, γνωστό και ως αρχείο διαμόρφωσης εικονικής μηχανής, είναι ένα αρχείο απλού κειμένου που χρησιμοποιείται από το λογισμικό εικονικοποίησης VMware για τον καθορισμό των ρυθμίσεων και των ρυθμίσεων της εικονικής μηχανής (VM). Τα αρχεία VMX περιέχουν πληροφορίες όπως η διαμόρφωση υλικού του VM, αντιστοιχίσεις εικονικού δίσκου, ρυθμίσεις δικτύου και άλλες παραμέτρους.

## Παράδειγμα αρχείου VMX

Ακολουθεί ένα παράδειγμα του πώς μπορεί να μοιάζει το αρχείο VMX:

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## Τι περιέχει το αρχείο VMX;

Ένα αρχείο VMX περιέχει διάφορες ρυθμίσεις διαμόρφωσης για εικονική μηχανή (VM). Ακολουθούν ορισμένες από τις ρυθμίσεις που βρίσκονται συνήθως στο αρχείο VMX:

- `.encoding:` Καθορίζει την κωδικοποίηση χαρακτήρων που χρησιμοποιείται στο αρχείο.
- `config.version:` Υποδεικνύει την έκδοση της μορφής αρχείου VMX.
- `virtualHW.version:` Καθορίζει την έκδοση του εικονικού υλικού για το VM.
- `guestOS:` Καθορίζει το λειτουργικό σύστημα επισκέπτη που είναι εγκατεστημένο στο VM.
- `memSize:` Καθορίζει την ποσότητα μνήμης που εκχωρείται στο VM.
- `displayName:` Ορίζει το εμφανιζόμενο όνομα ή ετικέτα για το VM.
- `PowerType:` Καθορίζει τη συμπεριφορά ισχύος για διαφορετικές λειτουργίες (απενεργοποίηση, ενεργοποίηση, επαναφορά, αναστολή).
- `floppyX:` Ρυθμίσεις διαμόρφωσης που σχετίζονται με μονάδες δισκέτας, όπως αντιστοιχίσεις παρουσίας και αρχείων.
- `numvcpus:` Καθορίζει τον αριθμό των εικονικών CPU που έχουν εκχωρηθεί στο VM.
- `scsiX:` Ρυθμίσεις διαμόρφωσης για ελεγκτές SCSI και τους σχετικούς εικονικούς δίσκους.
- `ethernetX:` Ρυθμίσεις διαμόρφωσης για προσαρμογείς δικτύου, συμπεριλαμβανομένου του τύπου εικονικής συσκευής, του ονόματος δικτύου και του τύπου διεύθυνσης.
- `ideX:` Ρυθμίσεις διαμόρφωσης για ελεγκτές IDE και τους σχετικούς εικονικούς δίσκους.
- `usbX:` Ρυθμίσεις διαμόρφωσης για συσκευές USB, όπως στοιχεία παρουσίας και σύνδεσης.
- `sound:` Ρυθμίσεις διαμόρφωσης για τον εικονικό προσαρμογέα ήχου.
- `tools.syncTime:` Υποδεικνύει εάν είναι ενεργοποιημένος ο συγχρονισμός ώρας με το κεντρικό σύστημα.
- `uuid.bios:` Καθορίζει το BIOS UUID του VM.
- `uuid.location:` Καθορίζει την τοποθεσία UUID του VM.

## Πώς να ανοίξετε το αρχείο VMX;

Το μη αυτόματο άνοιγμα ενός αρχείου VMX δεν συνιστάται. Όταν εκτελείτε μια εικονική μηχανή χρησιμοποιώντας το VMware Fusion, το λογισμικό φορτώνει αυτόματα τις πληροφορίες από το αρχείο VMX.

Ωστόσο, εάν θέλετε να επεξεργαστείτε μη αυτόματα το αρχείο VMX, μπορείτε να το κάνετε χρησιμοποιώντας οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου, π.χ. Σημειωματάριο (Windows) ή TextEdit (Mac).

## Ποια είναι η μορφή του αρχείου VMX;

Ένα αρχείο VMX είναι ένα αρχείο απλού κειμένου με συγκεκριμένη μορφή. Η μορφή ακολουθεί μια δομή ζεύγους κλειδιού-τιμής όπου κάθε γραμμή αντιπροσωπεύει ξεχωριστή επιλογή διαμόρφωσης.

Η γενική μορφή του αρχείου VMX είναι η εξής:

```
key1 = value1
key2 = value2
key3 = value3
```

Κάθε γραμμή αποτελείται από κλειδί που ακολουθείται από το σύμβολο ίσου (=) και την αντίστοιχη τιμή. Το κλειδί αντιπροσωπεύει μια συγκεκριμένη ρύθμιση διαμόρφωσης και η τιμή αντιπροσωπεύει την τιμή που έχει εκχωρηθεί σε αυτήν τη ρύθμιση.

Για παράδειγμα, το `memSize = "8192"` στο αρχείο VMX καθορίζει ότι το όριο μνήμης της εικονικής μηχανής είναι 8192 MB μνήμης RAM.

Η μορφή του αρχείου VMX μπορεί επίσης να περιλαμβάνει σχόλια, που υποδηλώνονται με ένα σύμβολο λίρας (#) στην αρχή της γραμμής, τα οποία αγνοούνται από το λογισμικό VMware κατά την ανάλυση του αρχείου. Τα σχόλια χρησιμοποιούνται συχνά για την παροχή πρόσθετων πληροφοριών ή επεξηγήσεων για συγκεκριμένες ρυθμίσεις.

## βιβλιογραφικές αναφορές
* [Δείγμα αρχείου VMX](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)



