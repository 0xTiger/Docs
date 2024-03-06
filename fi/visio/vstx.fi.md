{
  "date" : "2019-10-11",
  "keywords" : [ "vstx file", "vstx file format", "what is a vstx file", "file", "vstx example", "vstx file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSTX - Microsoft Visio -tiedostomuoto",
  "description":"Opi VSTX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VSTX-tiedostoja.",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx-fi",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Mikä on VSTX-tiedosto?

Tiedostot, joiden laajennus on .vstx, ovat piirustusmallitiedostoja, jotka on luotu Microsoft Visio 2013:lla tai uudemmalla. Nämä VSTX-tiedostot tarjoavat lähtökohdan [.VSDX](/visio/vsdx/)-tiedostoina tallennettujen Visio-piirustusten luomiseen oletusasettelulla ja -asetuksilla. Yleensä Visio-tiedostoja käytetään luomaan piirustuksia, jotka sisältävät visuaalisia objekteja, vuokaavioita, UML-kaavioita, tietokulkuja, organisaatiokaavioita, ohjelmistokaavioita, verkkoasetteluja, tietokantamalleja, objektikartoitusta ja muuta vastaavaa tietoa. Visiolla luodut tiedostot voidaan myös viedä eri tiedostomuotoihin, kuten [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) ja muihin. VSTX-tiedostoja avaaviin ohjelmiin kuuluu Microsoft Visio for Windows ja Mac, jonka avulla voit avata nämä tiedostot katselua ja muokkausta varten. Sen avulla voidaan myös muuntaa Visio-tiedostomuotoja useisiin muihin muotoihin.

# VSTX tiedostomuoto #

X tiedostopäätteessä viittaa OpenOffice-tiedostomuotoon, jonka Microsoft esitteli [ZIP](/compression/zip/)-arkistotiedostomuotona, joka korvaa aiemmin tuetut binaaritiedostomuodot. VSTX-tiedostot perustuvat siten OpenOffice-määritysten XML-tiedostomuotoon, toisin kuin [.VST](/visio/vst/)-tiedostomuoto, joka on binäärimuodossa.

VSDX-tiedostot perustuvat Open Packaging Conventions ja XML:ään, ja kehittäjät voivat hyötyä tästä muodosta oppimalla käsittelemään näitä tiedostoja ohjelmallisesti. Muoto perii monia samoja XML-rakenteita kuin sen osat Visio XML Drawing -tiedostomuodosta (.vdx). Yhteentoimivuus Visio-tiedostojen kanssa on lisääntynyt huomattavasti, koska kolmannen osapuolen ohjelmistot voivat käsitellä Visio-tiedostoja tiedostomuototasolla.

Tietyt muut Visio 2013 -tiedostomuodon muodostavat tiedostotyypit ovat:

* .vsdm (Visio-makroa tukeva piirustus)

* .vssx (Visio-stensiili)

* .vssm (Visio-makroa tukeva malli)

* .vstx (Visio-malli)

* .vstm (Visio-makroa tukeva malli)


Kotelon alla oleva Visio 2013 -tiedostomuoto käyttää strukturoitua tapaa tallentaa sovellustiedot ja niihin liittyvät resurssit arkistoon, kuten {{HYPERLINKKI}}. ZIP-tiedosto voidaan purkaa millä tahansa tavallisella purkuohjelmalla, jossa se sisältää myös muun tyyppisiä tiedostoja. Voit vain korvata .VSTX-tiedostotunnisteen .ZIP:llä Windows Explorerissa nähdäksesi VSTX-tiedoston sisällön.

Jokaista Visio-tiedostoa kutsutaan paketiksi, joka sisältää muita tiedostoja tai osia. Paketin osa voi olla XML-tiedosto, kuva tai jopa VBA-ratkaisu. Paketin sisältämät osat voidaan jakaa asiakirja- ja suhde-osiin.

### Asiakirja ###

Asiakirjan osat sisältävät Visio-tiedoston todellisen sisällön ja metatiedot, kuten tiedoston nimen, ensimmäisen sivun ja kaikki sen sisältämät muodot sekä jopa muotojen tietoyhteydet. Paketissa olevat kuvat ja tekstitiedostot katsotaan asiakirjan osiksi.

### Suhteet ###

Visio-tiedoston suhdeosat tallennetaan _rels-kansioon, ja ne kuvaavat, kuinka paketin osat liittyvät kuhunkin. Se tarjoaa myös tiedoston rakenteen. Itsenäinen XML-dokumentti käyttää elementtien ylä- ja alasuhdetta määrittääkseen entiteettien suhteen toisiinsa. Kelvollinen Visio 2013 -tiedostomuoto sisältää oikean joukon osia ja paketti sisältää osien väliset suhteet.

Suhdeosat ovat XML-dokumentteja, jotka kuvaavat paketin eri asiakirjaosien välisiä suhteita. Ne määrittelevät yhteyden kahden kohteen välillä: määritetyn lähteen (määritetty suhdetiedoston nimen ja sijainnin mukaan) ja määritetyn kohdeasiakirjan osan. Suhdeosia käytetään esimerkiksi kuvaamaan, mitkä muotopohjat liittyvät tiedostoon, kuinka sivut liittyvät tiedostoon ja toisiinsa tai miten kuvat ja objektit liittyvät tiettyyn sivuun.

## Viitteet ##

* [Johdatus Visio-tiedostomuotoon](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

