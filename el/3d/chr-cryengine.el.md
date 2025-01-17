{
"ημερομηνία":"2023-10-11",
   "keywords":[
"chr",
"αρχείο chr",
"αρχείο χαρακτήρων chr cryengine",
"πώς να ανοίξετε ένα αρχείο chr",
"αρχείο",
"επέκταση αρχείου chr",
"επέκταση",
"αρχείο"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"ψευδές",
"toc":true,
"title":"Μορφή αρχείου CHR - Αρχείο χαρακτήρων CryENGINE",
   "description":"Μάθετε σχετικά με τη μορφή αρχείου χαρακτήρων CHR CryENGINE και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CHR.",
"linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Τι είναι ένα αρχείο CHR;

Το αρχείο CHR στο πλαίσιο του CryENGINE αναφέρεται σε ένα **Αρχείο χαρακτήρων CryENGINE**. Το CryENGINE είναι μηχανή παιχνιδιών που αναπτύχθηκε από την Crytek και αυτά τα αρχεία χρησιμοποιούνται για την αποθήκευση μοντέλων χαρακτήρων και σχετικών δεδομένων για χρήση σε βιντεοπαιχνίδια και άλλες εφαρμογές σε πραγματικό χρόνο.

## Αρχείο χαρακτήρων CryENGINE

Ένα αρχείο χαρακτήρων CryENGINE περιέχει συνήθως τα ακόλουθα στοιχεία:

1. **Μοντέλο χαρακτήρων**: Πρόκειται για τρισδιάστατο μοντέλο χαρακτήρων, συμπεριλαμβανομένης της γεωμετρίας, των υφών και των κινούμενων εικόνων του. Αυτά τα μοντέλα δημιουργούνται συχνά χρησιμοποιώντας λογισμικό όπως το Autodesk Maya ή το Blender και στη συνέχεια εισάγονται στο CryENGINE.
    




















2. **Δεδομένα κινούμενων σχεδίων**: Το CryENGINE υποστηρίζει πολύπλοκα κινούμενα σχέδια για χαρακτήρες, επομένως το αρχείο ".chr" μπορεί να περιλαμβάνει διάφορα κινούμενα σχέδια όπως περπάτημα, τρέξιμο, άλμα και άλλα. Αυτά τα κινούμενα σχέδια αποθηκεύονται συνήθως ως δεδομένα βασικού καρέ.
    




















3. **Πληροφορίες εξάρτισης**: Η εξάρθρωση αναφέρεται στη διαδικασία δημιουργίας δομής σκελετού για μοντέλο χαρακτήρων, η οποία επιτρέπει την εφαρμογή κινούμενων εικόνων στο μοντέλο. Το αρχείο ".chr" μπορεί να περιέχει πληροφορίες σχετικά με την ιεραρχία των οστών και τον τρόπο με τον οποίο το πλέγμα του χαρακτήρα συνδέεται με αυτόν τον σκελετό.
    




















4. **Δεδομένα υλικού και υφής**: Πληροφορίες σχετικά με υλικά που χρησιμοποιούνται στο μοντέλο χαρακτήρων και στους σχετικούς χάρτες υφής ενδέχεται να περιλαμβάνονται στο αρχείο ".chr". Το CryENGINE υποστηρίζει φυσική απόδοση, επομένως αυτά τα υλικά μπορούν να είναι αρκετά λεπτομερή.
    




















5. **Δεδομένα φυσικής**: Εάν ο χαρακτήρας προορίζεται να αλληλεπιδράσει με τον κόσμο του παιχνιδιού, το αρχείο ".chr" μπορεί να περιλαμβάνει δεδομένα φυσικής, όπως σχήματα σύγκρουσης ή περιορισμούς για τη φυσική κούκλα.
    




















6. **Ρυθμίσεις διαμόρφωσης**: Διάφορες ρυθμίσεις διαμόρφωσης που σχετίζονται με τη συμπεριφορά των χαρακτήρων στον κόσμο του παιχνιδιού, όπως η συμπεριφορά τεχνητής νοημοσύνης ή τα σενάρια συμβάντων, μπορεί επίσης να αποτελούν μέρος του αρχείου ".chr".

## CryENGINE

Το CryENGINE είναι μια ισχυρή μηχανή παιχνιδιών που αναπτύχθηκε από την Crytek, γερμανική εταιρεία βιντεοπαιχνιδιών. Είναι γνωστό για τις πρωτοποριακές του δυνατότητες γραφικών και έχει χρησιμοποιηθεί για τη δημιουργία μερικών οπτικά εντυπωσιακών και τεχνολογικά προηγμένων βιντεοπαιχνιδιών. Ακολουθούν ορισμένα βασικά χαρακτηριστικά και πληροφορίες σχετικά με το CryENGINE:

1. **Γραφικά και απόδοση**: Η CryENGINE είναι γνωστή για τις προηγμένες δυνατότητες γραφικών της. Υποστηρίζει λειτουργίες όπως παγκόσμιος φωτισμός σε πραγματικό χρόνο, δυναμικός φωτισμός και σκιές υψηλής ποιότητας, απόδοση φυσικής βάσης (PBR) και υφές υψηλής ανάλυσης. Αυτά τα χαρακτηριστικά συμβάλλουν στη δημιουργία οπτικά εντυπωσιακών και ρεαλιστικών κόσμων παιχνιδιών.
    




















2. **Physics Engine**: Το CryENGINE περιλαμβάνει ενσωματωμένη μηχανή φυσικής που επιτρέπει ρεαλιστικές αλληλεπιδράσεις μεταξύ αντικειμένων στον κόσμο του παιχνιδιού. Υποστηρίζει χαρακτηριστικά όπως το άκαμπτο σώμα, τη φυσική του μαλακού σώματος και το ragdoll physics, καθιστώντας το κατάλληλο για τη δημιουργία δυναμικών και καθηλωτικών περιβαλλόντων.
    




















3. **Έδαφος και βλάστηση**: Το CryENGINE παρέχει εργαλεία για τη δημιουργία τεράστιου και λεπτομερούς εξωτερικού περιβάλλοντος. Υποστηρίζει επεξεργασία εδάφους, τοποθέτηση βλάστησης και δυναμικά καιρικά συστήματα, επιτρέποντας στους προγραμματιστές να δημιουργήσουν εκτεταμένες και ρεαλιστικές ρυθμίσεις εξωτερικού χώρου.
    




















4. **Κινούμενη εικόνα χαρακτήρων**: Το CryENGINE περιλαμβάνει ισχυρά εργαλεία για κινούμενα σχέδια χαρακτήρων. Υποστηρίζει πολύπλοκα rigs χαρακτήρων, κινούμενα σχέδια προσώπου και σύστημα blend tree που επιτρέπει στους προγραμματιστές να δημιουργούν ρεαλιστικές κινήσεις χαρακτήρων και κινούμενα σχέδια.
    




















5. **Σύστημα AI**: Ο κινητήρας διαθέτει σύστημα τεχνητής νοημοσύνης που επιτρέπει τη δημιουργία έξυπνων NPC (χαρακτήρες που δεν είναι παίκτες) και εχθρικού AI. Οι προγραμματιστές μπορούν να γράψουν τη συμπεριφορά και τις αλληλεπιδράσεις AI για να δημιουργήσουν προκλητικές και καθηλωτικές εμπειρίες παιχνιδιού.
       





















6. **Scripting**: Το CryENGINE χρησιμοποιεί γλώσσα δέσμης ενεργειών που ονομάζεται "Schematyc" που επιτρέπει στους προγραμματιστές να δημιουργούν λογική παιχνιδιού και αλληλεπιδράσεις. Επιπλέον, υποστηρίζει C++ για πιο προηγμένες ανάγκες προγραμματισμού.

## Μορφές αρχείων που χρησιμοποιούνται από την CryENGINE

Ακολουθούν ορισμένοι από τους κοινούς τύπους αρχείων που σχετίζονται με το CryENGINE:

1. **cryproj**: Αρχεία έργου CryENGINE. Αυτά τα αρχεία αποθηκεύουν ρυθμίσεις και διαμορφώσεις για συγκεκριμένο έργο για συγκεκριμένο έργο παιχνιδιού.
    




















2. **.level**: Τα αρχεία επιπέδου περιέχουν δεδομένα τρισδιάστατου κόσμου παιχνιδιών, συμπεριλαμβανομένου του εδάφους, των αντικειμένων, του φωτισμού και άλλων ρυθμίσεων για συγκεκριμένο επίπεδο. Τα επίπεδα είναι θεμελιώδες στοιχείο του σχεδιασμού του παιχνιδιού στο CryENGINE.
    




















3. **.cgf**: Μορφή γεωμετρίας χαρακτήρων. Αυτά τα αρχεία περιέχουν δεδομένα τρισδιάστατου μοντέλου για χαρακτήρες, αντικείμενα και άλλα στοιχεία του παιχνιδιού. Τα αρχεία CGF μπορούν να περιλαμβάνουν δεδομένα γεωμετρίας, υφές και κινούμενα σχέδια.
    




















4. **.chrparams**: Αρχεία παραμέτρων χαρακτήρων. Αυτά τα αρχεία αποθηκεύουν ρυθμίσεις και διαμορφώσεις για μοντέλα χαρακτήρων και τα κινούμενα σχέδια τους.
    




















5. **.dds**: Μορφή υφής DirectX. Το CryENGINE χρησιμοποιεί συνήθως αρχεία DDS για την αποθήκευση υφών, συμπεριλαμβανομένων των διάχυτων χαρτών, των κανονικών χαρτών και άλλων τύπων υφής.
    




















6. **.cryshader**: Αρχεία Shader CryENGINE. Αυτά τα αρχεία καθορίζουν τον τρόπο απόδοσης των υλικών και των αντικειμένων στον κόσμο του παιχνιδιού, προσδιορίζοντας shaders, ιδιότητες υλικού και άλλα.
    




















7. **.crytif**: Αρχείο πληροφοριών υφής. Αυτά τα αρχεία αποθηκεύουν πρόσθετες πληροφορίες σχετικά με τις υφές, όπως ρυθμίσεις συμπίεσης, mipmaps και άλλες λεπτομέρειες που σχετίζονται με την υφή.
    




















8. **.cdf**: Αρχείο ορισμού χαρακτήρων. Τα αρχεία CDF χρησιμοποιούνται για τον καθορισμό των στοιχείων χαρακτήρων και των ιδιοτήτων τους, συμπεριλαμβανομένων των συνημμένων, των καταστάσεων κινούμενων εικόνων και των ρυθμίσεων που σχετίζονται με χαρακτήρες.
    




















9. **.dds**: Το CryENGINE χρησιμοποιεί επίσης αρχεία DDS (DirectDraw Surface) για διάφορους χάρτες υφής, όπως κανονικούς χάρτες, κατοπτρικούς χάρτες και διάχυτους χάρτες.
    




















10. **.anim**: Αρχεία κινούμενων εικόνων. Αυτά τα αρχεία αποθηκεύουν δεδομένα κινούμενων εικόνων για χαρακτήρες και αντικείμενα, συμπεριλαμβανομένων των βασικών καρέ, των θέσεων των οστών και των ακολουθιών κινούμενων εικόνων.
    




















11. **.xml**: Τα αρχεία XML μπορούν να χρησιμοποιηθούν για διάφορες διαμορφώσεις και ορισμούς δεδομένων στο CryENGINE, όπως η λογική του παιχνιδιού, η συμπεριφορά AI και άλλα.
    




















12. **.pak**: Τα [PAK files](/el/game/pak/) είναι αρχεία αρχειοθέτησης που χρησιμοποιούνται για τη συσκευασία περιουσιακών στοιχείων και πόρων παιχνιδιού, καθιστώντας το πιο αποτελεσματικό για τη διανομή και τη φόρτωση του παιχνιδιού.

## Πώς να ανοίξετε το αρχείο CHR;

Τα προγράμματα που ανοίγουν αρχεία CHR περιλαμβάνουν

- **Crytek CryENGINE SDK** (Δωρεάν δοκιμή) για Windows

**Υποτύπος:** Αρχεία εικόνας 3D

## Άλλα αρχεία CHR

Ακολουθούν άλλοι τύποι αρχείων που χρησιμοποιούν την επέκταση αρχείου **.chr**.

**3D**
- [CHR - Αρχείο χαρακτήρων CryENGINE](/el/3d/chr-cryengine/)
- [CHR - Αρχείο χαρακτήρων 3ds Max](/el/3d/chr-3ds/)

**Γραμματοσειρά και παιχνίδι**
- [CHR - Σύνολο χαρακτήρων Borland](/el/font/chr/)
- [CHR - Doki Doki Literature Club! Αρχείο χαρακτήρων](/el/game/chr-doki/)

## βιβλιογραφικές αναφορές
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

