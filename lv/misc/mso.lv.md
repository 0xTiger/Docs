{
  "date": "2022-03-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSO — Microsoft Office makro atsauces fails",
  "description": "Uzziniet par MSO failiem un API, kas var izveidot un atvērt MSO failus.",
  "linktitle": "MSO",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-ms-lvo"
}
},
  "lastmod": "2022-03-12"
}

## Kas ir MSO fails?

An MSO file is a data container file format that is created when an HTML message is sent using Microsoft Outlook. This happens mostly with Microsoft Office 2000 applications. In most of the cases, the email message is attached with the name **Oledata.mso** file. The email recipient, when opens such an email, can view the file correctly even if they don't have the same software installed. MSO files refer to [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Microsoft MSO faila formāts

MSO faili tiek saglabāti Microsoft Compound Document File Format (MCDF), kas ir pazīstams arī kā objektu saistīšanas un iegulšanas (OLE) vai komponentu objektu modeļa (COM) strukturētās krātuves saliktā faila ieviešanas binārā faila formātā.

### MSO faila formāta struktūra

The internal file format structure of MSO file format is well-defined in the [Structures](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd) section of MCDF documentation.  The File Allocation Table (FAT) manages the sector allocation and sector chains. It contains an array of 32-bit sector numbers. Each index in the array represents a sector number whereas its value represents the next sector in the chain or a special value.

## Atsauces

* [COM strukturētā krātuve](https://en.wikipedia.org/wiki/COM_Structured_Storage)

* [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

