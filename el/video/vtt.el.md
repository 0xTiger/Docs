---
date: 2022-01-06
keywords: vtt, .vtt, μορφή αρχείου vtt, μορφή αρχείου .vtt, επέκταση .vtt, επέκταση vtt
συγγραφέας:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Μάθετε για το αρχείο .vtt και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία VTT."
title: Μορφή αρχείου VTT - Αρχείο κομματιών κειμένου βίντεο Ιστού
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Τι είναι ένα αρχείο VTT;

Ένα αρχείο VTT είναι ένα αρχείο κειμένου που περιέχει πληροφορίες για την εμφάνιση κομματιών κειμένου με χρονική διάρκεια (όπως υπότιτλους ή λεζάντες) χρησιμοποιώντας τη μορφή κομματιών κειμένου βίντεο Web (WebVTT). Τα χρονομετρημένα κομμάτια κειμένου περιλαμβάνουν πληροφορίες όπως υπότιτλους ή λεζάντες. Ο σκοπός του αρχείου VTT είναι να προσθέσει επικαλύψεις κειμένου σε α<video> . Η μορφή είναι κάπως παρόμοια με τα αρχεία SRT. Τα αρχεία κειμένου που βασίζονται στο WebVTT κωδικοποιούνται χρησιμοποιώντας UTF-8. Ένα αρχείο VTT περιέχει πληροφορίες όπως υπότιτλους, περιγραφές, λεζάντες, περιγραφές, κεφάλαια και μεταδεδομένα. Όντας αρχεία απλού κειμένου, τα αρχεία VTT μπορούν να ανοίξουν χρησιμοποιώντας προγράμματα επεξεργασίας κειμένου όπως το Microsoft Notepad, το Apple TextEdit και το Notepad++.

## Μορφή αρχείου VTT - Περισσότερες πληροφορίες

Τα αρχεία VTT χρησιμοποιούν τη μορφή αρχείου WebVTT για την αποθήκευση πληροφοριών διαδοχικών κομματιών κειμένου. Κάθε κομμάτι κειμένου χρονομετρημένου αποτελείται από μία γραμμή ή πολλαπλές γραμμές, επίσης γνωστή ως «σύνδειξη», όπως φαίνεται στο ακόλουθο παράδειγμα.

### Παράδειγμα αρχείου VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### Δομή αρχείου VTT

Ακολουθούν οι απαιτήσεις δομής ενός αρχείου VTT.

* Ένα προαιρετικό σήμα παραγγελίας byte (BOM).
* Η συμβολοσειρά "WEBVTT".
* Μια προαιρετική κεφαλίδα κειμένου στα δεξιά του WEBVTT.
* Μια κενή γραμμή, η οποία ισοδυναμεί με δύο διαδοχικές νέες γραμμές.
* Μηδέν ή περισσότερα στοιχεία ή σχόλια.
* Μηδέν ή περισσότερες κενές γραμμές.

## βιβλιογραφικές αναφορές

* [VTT - W3 Schools](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

