{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XFDF-filformat - Hvad er en XFDF-fil?",
  "description": "Lær om XFDF-filer og API'er, der kan oprette og åbne XFDF-filer.",
  "linktitle": "XFDF",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-xfd-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en XFDF fil?

A file with .xfdf extension is an XML Forms Data Format that is generated with Adobe Acrobat software. Like [FDF](/pdf/fdf/), XFDF contains form elements description and their values in XML format. This can include the names and values of text fields in the PDF form. XFDF are saved in human-readable format and can be read programatically read using programming languages such as C#.

## XFDF-filformat - flere oplysninger

XFDF-filer gemmes i XML-filformat, der er et universelt format, der bruges til import og eksport af data. En XFDF-filstruktur består af en header efterfulgt af feltværdier og elementdata som vist nedenfor.

|Element|Attribut|Indhold|
---|---|---|
|\<XFDF> ||Øverste element|
|\<fields> ||Alle feltværdier for denne skabelon|
|<field (T)> |navn |Feltnavn|
|<value (V)> |værdi |Feltværdi|

## Referencer

* [FDF Format Support by Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)

* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)
