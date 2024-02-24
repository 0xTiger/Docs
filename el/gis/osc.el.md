{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Αλλαγή μορφής αρχείου",
  "description":"Μάθετε για τη μορφή αρχείου OSC και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία OSC.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-el",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Τι είναι ένα αρχείο OSC;

Ένα αρχείο OSC είναι μια αλλαγή μορφής αρχείου που περιέχει τροποποιημένα δεδομένα οδικού χάρτη για έναν υπάρχοντα οδικό χάρτη .osm. Περιέχει πληροφορίες σχετικά με τις αλλαγές που πρέπει να γίνουν στο [OSM file](/gis/osm/). Το αρχείο OSC μπορεί να έχει τρεις πιθανούς τύπους λειτουργιών τροποποίησης σε δεδομένα OSM, π.χ. «εισαγωγή», «τροποποίηση» ή «διαγραφή». Αυτά τα αρχεία αλλαγών χρησιμοποιούνται συνήθως για την εξαγωγή δεδομένων από το πρόγραμμα επεξεργασίας OSM και την εισαγωγή σε άλλο πρόγραμμα επεξεργασίας.

Μπορείτε να ανοίξετε αρχεία OSC με το λογισμικό Merkaartar και osmchange.

## Μορφή αρχείου OSC

Τα αρχεία OSC αποθηκεύονται συνήθως σε μορφή αρχείου JOSM όπου οι αλλαγές αντιπροσωπεύονται από ετικέτες. Ξεκινά με την ετικέτα «osmChange» που υποδεικνύει την αρχή του αρχείου. Οι δευτερεύουσες ετικέτες καθορίζουν εάν πρόκειται για λειτουργία εισαγωγής, τροποποίησης ή διαγραφής που πρόκειται να εκτελεστεί στον αντίστοιχο κόμβο στο αρχείο OSM. Τα περιεχόμενα ενός κόμβου περιέχουν στην πραγματικότητα τα περιεχόμενα μιας ετικέτας osm.

### Παράδειγμα μορφής αρχείου OSC

Ακολουθεί ένα παράδειγμα λειτουργίας τροποποίησης σε έναν κόμβο. Κάθε στοιχείο πρέπει να έχει ένα αναγνωριστικό συνόλου αλλαγών και έναν αριθμό έκδοσης.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## βιβλιογραφικές αναφορές

* [Μορφή αρχείου JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format)

