{
  "date": "2021-03-23",
  "keywords": [
"NCX",
"Comhad XML um Rialú Nascleanúna EPUB",
"síneadh",
"formáid",
"E-Leabhar",
"TOC",
"Cuibhreannas DAISY"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi bhformáid comhaid XML (NCX) Comhad XML um Rialú Nascleanúna EPUB agus APIanna ar féidir leo comhaid NCX a chruthú agus a oscailt.",
  "title": "NCX - EPUB Rialú Nascleanúna Comhad XML",
  "linktitle": "NCX",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-ncx"
}
},
  "lastmod": "2021-03-22"
}

## Cad is comhad NCX ann? ##

Giorraíodh an comhad NCX mar chomhad Rialaithe Nascleanúna le haghaidh XML, ar a dtugtar de ghnáth toc.ncx. Is éard atá sa chomhad seo an tábla ordlathach ábhar do chomhad EPUB. Forbraíodh an tsonraíocht don NCX don Leabhar Cainte Digiteach (DTB) agus coimeádann **DAISY Consortium** an fhormáid comhaid seo agus ní cuid de shonraíocht EPUB í. Cuimsíonn an comhad NCX cineál míme de **app/x-dtbncx+xml** isteach ann.

## Sonraíocht NCX ##

The NCX file contains various kinds of XML tags. The meta tags like `meta name="dtb:uid"` is used to mention the ID. The `meta name="d-gatb:depth"` element is set equal to the depth of the `navMap` tag element. The `navPoint` elements can be nested to create a hierarchical table of contents. The content of `navLabel` is the text that appears in the table of contents generated by reading systems that use the .ncx. The content of `navPoint` element points to a content document listed in the manifest and can also include an element identifier 

A description of certain exceptions to the NCX specification as used in EPUB. Here you can view the example of an NCX file:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ncx PUBLIC "-//NISO//DTD ncx 2005-1//EN"
"http://www.daisy.org/z3986/2005/ncx-2005-1.dtd">

<ncx version="2005-1" xml:lang="en" xmlns="http://www.daisy.org/z3986/2005/ncx/">

  <head>
<!-- The following four metadata items are required for all NCX documents,
including those that conform to the relaxed constraints of OPS 2.0 -->

    <meta name="dtb:uid" content="123456789X"/> <!-- same as in .opf -->
    <meta name="dtb:depth" content="1"/> <!-- 1 or higher -->
    <meta name="dtb:totalPageCount" content="0"/> <!-- must be 0 -->
    <meta name="dtb:maxPageNumber" content="0"/> <!-- must be 0 -->
  </head>

  <docTitle>
    <text>Pride and Prejudice</text>
  </docTitle>

  <docAuthor>
    <text>Austen, Jane</text>
  </docAuthor>

  <navMap>
    <navPoint class="chapter" id="chapter1" playOrder="1">
      <navLabel><text>Chapter 1</text></navLabel>
      <content src="chapter1.xhtml"/>
    </navPoint>
  </navMap>

</ncx>
```

## Tagairtí ##

* [EPUB Ón Vicipéid](https://en.wikipedia.org/wiki/EPUB)

* [What files to include in the toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

