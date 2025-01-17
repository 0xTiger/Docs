{
  "date" : "2021-01-20",
  "keywords" :["xslt", "File", "Extension", "File Format", "File Extension", "Extensible Style Sheet Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου XSLT",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου XSLT και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία XSLT.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## Τι είναι ένα αρχείο XSLT;

Ένα αρχείο με επέκταση .xslt είναι ένα αρχείο μετατροπής γλώσσας επεκτάσιμου φύλλου στυλ που χρησιμοποιείται για τον μετασχηματισμό και το στυλ ενός αρχείου XML χρησιμοποιώντας οδηγίες XSL. Η μορφή χρησιμοποιείται για τη μετατροπή εγγράφων XML σε τυπικές μορφές εξόδου, όπως ένα έγγραφο κειμένου ή μια ιστοσελίδα .html. Αυτός ο μετασχηματισμός δημιουργεί ένα νέο έγγραφο με βάση το περιεχόμενο του υπάρχοντος εγγράφου XML. Το XSLT το καθιστά θεωρητικά ικανό για αυθαίρετους υπολογισμούς.

## Μορφή αρχείου XSLT

Η μορφή αρχείου XLST περιέχει οδηγίες μετασχηματισμού σε μορφή απλού κειμένου που μπορούν να προβληθούν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου. Έχουν γίνει τρεις αναθεωρήσεις στη γλώσσα.

* «XSLT 1.0» - Το XSLT 1.0 δημοσιεύτηκε ως σύσταση του W3C τον Νοέμβριο του 1999.
* `XSLT 2.0` - Περιλαμβάνει τροποποιήσεις όπως χειραγώγηση συμβολοσειρών με χρήση κανονικών εκφράσεων, συναρτήσεων και τελεστών για τον χειρισμό ημερομηνιών, ωρών και διάρκειων, πολλαπλών εγγράφων εξόδου, ομαδοποίηση και ένα πιο πλούσιο σύστημα τύπων και ισχυρό έλεγχο τύπων.
* `XSLT 3.0` - Έγινε μέρος της Σύστασης του W3C στις 8 Ιουνίου 2017 και οι κύριες νέες δυνατότητες περιλαμβάνουν μετασχηματισμό ροής, πακέτα για τη βελτίωση της αρθρωτής διαμόρφωσης μεγάλων φύλλων στυλ, βελτιωμένο χειρισμό δυναμικών σφαλμάτων με, για παράδειγμα, μια οδηγία xsl:try, και υποστήριξη για χάρτες και πίνακες, επιτρέποντας στο XSLT να χειρίζεται JSON καθώς και XML.

### Παράδειγμα XSLT

Το παρακάτω παράδειγμα λαμβάνεται από το [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## Βιβλιογραφικές αναφορές ##

* [XSLT - Από τη Wikipedia](https://en.wikipedia.org/wiki/XSLT)
* [XSLT Elements](https://en.wikipedia.org/wiki/XSLT_elements)

