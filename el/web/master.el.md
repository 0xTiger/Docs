{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Αρχείο MASTER - Μορφή αρχείου κύριας σελίδας ASP.NET",
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου MASTER και τα API για τη δημιουργία και το άνοιγμα αρχείων MASTER.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Τι είναι ένα αρχείο MASTER;

Ένα αρχείο MASTER είναι ένα αρχείο προτύπου κύριας ιστοσελίδας που δημιουργήθηκε με το ASP.NET. Χρησιμοποιείται ως σημείο εκκίνησης για τη δημιουργία πολλών σελίδων που έχουν την ίδια διάταξη και ρυθμίσεις με το αρχείο MASTER. Το πρότυπο αρχείο MASTER περιλαμβάνει ρυθμίσεις για κεφαλίδα, μενού πλοήγησης, υποσέλιδο, γραμματοσειρά και πληροφορίες στυλ. Η χρήση ενός αρχείου MASTER βοηθά στη γρήγορη δημιουργία πολλών ιστοσελίδων.

Μπορείτε να ανοίξετε ένα αρχείο MASTER χρησιμοποιώντας το Microsoft Visual Studio 2022 και νεότερη έκδοση.

## Μορφή αρχείου MASTER - Περισσότερες πληροφορίες

Ένα αρχείο MASTER δημιουργείται και αποθηκεύεται σε μορφή αρχείου HTML και είναι παρόμοιο με οποιοδήποτε άλλο αρχείο ιστοσελίδας. Είναι χωρισμένο σε επεξεργάσιμες και μη επεξεργάσιμες ενότητες. Οι επεξεργάσιμες ενότητες είναι αυτές που μπορούν να τροποποιηθούν ώστε να ανταποκρίνονται στις απαιτήσεις του χρήστη. Οι μη επεξεργάσιμες ενότητες είναι γκριζαρισμένες όταν ανοίγει το αρχείο MASTER στο Microsoft Visual Studio.

Οι κύριες σελίδες αποτελούνται από δύο κομμάτια, δηλαδή την ίδια την κύρια σελίδα και μία ή περισσότερες σελίδες περιεχομένου.

### Κύρια Σελίδα

Η κύρια σελίδα έχει επέκταση .master και είναι κατασκευασμένη σε ASP.NET. Έχει μια προκαθορισμένη διάταξη που αποτελείται από στατικό κείμενο, ετικέτες HTML και στοιχεία ελέγχου από την πλευρά του διακομιστή. Σε συνηθισμένες σελίδες .aspx, χρησιμοποιείται η οδηγία @ Page. Στην περίπτωση αρχείων .master, αυτό αντικαθίσταται από την οδηγία @ Master.

### Σελίδες περιεχομένου

Μια σελίδα περιεχομένου αντιπροσωπεύει το περιεχόμενο για τα στοιχεία ελέγχου κράτησης θέσης της κύριας σελίδας. Αυτές είναι σελίδες .aspx που είναι στην πραγματικότητα ο κώδικας πίσω από την κύρια σελίδα. Οι σελίδες περιεχομένου συνδέονται χρησιμοποιώντας την οδηγία Σελίδα @ συμπεριλαμβάνοντας ένα χαρακτηριστικό MasterPageFile που δείχνει στην κύρια σελίδα που θα χρησιμοποιηθεί όπως φαίνεται παρακάτω.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## βιβλιογραφικές αναφορές

* [Επισκόπηση Κύριων Σελίδων ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))
