{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CUBE fails - Gaussian Cube fails - Kas ir .cube fails un kā to atvērt?",
  "description" : "Uzziniet par Gausa kuba failu un to, kā to atvērt.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-cube-lv",
      "parent" : "data"
}
},
  "lastmod" : "2024-01-25"
}

## Kas ir CUBE fails?

CUBE faila formāts, kas pazīstams arī kā Gausa kuba fails (.cube), tiek izmantots skaitļošanas ķīmijā, lai saglabātu molekulāros datus, jo īpaši informāciju par elektronu blīvumu, kas iegūta kvantu ķīmijas aprēķinos. Šis formāts parasti tiek saistīts ar **Gausa programmatūras pakotni**, ko plaši izmanto elektronisko struktūru ab initio aprēķinu veikšanai.

Gausa kuba faili glabā trīsdimensiju datus, kas parasti atspoguļo elektronu blīvumu vai citas molekulu īpašības, kas iegūti, izmantojot kvantu ķīmijas aprēķinus. Failā ir galvenes sadaļa ar metadatiem (piemēram, izcelsme, datu punktu skaits pa katru asi un atstarpes), kam seko skaitlisko vērtību režģis, kas atspoguļo interesējošo īpašību (piemēram, elektronu blīvumu) katrā režģa punktā telpā.

Gausa kuba fails (.cube) ir vienkārša teksta fails ar noteiktu struktūru. Galvene satur informāciju par molekulāro sistēmu un datu režģi, un datu vērtības ir sakārtotas trīsdimensiju režģa formātā. Gausa kuba faili bieži tiek izmantoti, lai vizualizētu molekulārās īpašības, izmantojot molekulārās vizualizācijas programmatūru. Tādas programmas kā **VMD (Visual Molecular Dynamics)** vai **PyMOL** var nolasīt Gausa kuba failus, lai parādītu molekulārās virsmas, elektronu blīvumu vai citas aprēķinātās īpašības.

## Vienkāršots Gausa kuba faila piemērs:

```
Cubefile Example
Generated by Gaussian
  0  1  0  0  0  0  0  0  0  0
  0.0000000000000000E+00  0.0000000000000000E+00  0.0000000000000000E+00
 50  0.1000000000000000E+01  0.0000000000000000E+00  0.0000000000000000E+00
 50  0.0000000000000000E+00  0.1000000000000000E+01  0.0000000000000000E+00
 50  0.0000000000000000E+00  0.0000000000000000E+00  0.1000000000000000E+01
   0.123456789E+02  0.123456789E+02  0.123456789E+02  0.123456789E+02  0.123456789E+02
   ... (data values for electron density at each grid point)

```

## Par Gausu

Gaussian ir programmatūras lietojumprogrammu komplekts kvantu ķīmijai un skaitļošanas ķīmijai. Gausa galvenā uzmanība tiek pievērsta ab initio kvantu ķīmijas metodēm, kas ir ļoti precīzas, bet skaitļošanas ietilpīgas pieejas molekulu elektroniskās struktūras pētīšanai. Programmatūra tiek plaši izmantota pētniecībā un akadēmiskajos iestatījumos dažādiem lietojumiem, tostarp molekulāro īpašību prognozēšanai, reakcijas mehānismu izpētei un molekulāro struktūru izpētei.

## Par NWChem

NWChem ir atvērtā koda skaitļošanas ķīmijas programmatūra, kas paredzēta augstas veiktspējas kvantu ķīmijas simulācijām. Tas izmanto ab initio metodes, piemēram, Hartree-Fock un blīvuma funkcionālo teoriju, atbalsta paralēlo skaitļošanu, lai efektīvi veiktu aprēķinus par klasteriem, un atrod pielietojumu dažādās zinātnes jomās, tostarp skaitļošanas ķīmijā, bioķīmijā un materiālu zinātnē. NWChem ir pazīstams ar savu daudzpusību, ļaujot pētniekiem pētīt dažādas ķīmiskās sistēmas, un tā atvērtā koda būtība veicina kopienas ieguldījumu un pielāgošanu.

## Par VMD

VMD, kas apzīmē Visual Molecular Dynamics, ir jaudīga un plaši izmantota molekulārās vizualizācijas programma molekulārās dinamikas (MD) trajektoriju, kā arī statisku molekulāro struktūru attēlošanai, analīzei un animēšanai. Tas ir īpaši populārs skaitļošanas ķīmijas, molekulārās bioloģijas un strukturālās bioinformātikas jomās. VMD izceļas ar molekulāro struktūru vizualizēšanu, nodrošinot augstas kvalitātes molekulu un molekulāro kompleksu 3D atveidojumus. Tā atbalsta dažādus molekulāro failu formātus.

## Par PyMOL

PyMOL ir molekulārās vizualizācijas sistēma un programmatūras rīks, ko izmanto molekulāro struktūru trīsdimensiju vizualizācijai. Tas ir īpaši populārs strukturālās bioloģijas, bioinformātikas un skaitļošanas ķīmijas jomās. PyMOL nodrošina augstas kvalitātes molekulāro struktūru 3D atveidojumus, ļaujot lietotājiem vizualizēt un izpētīt bioloģisko makromolekulu formas, virsmas un mijiedarbību.

## Kā atvērt CUBE failu?

CUBE failu var atvērt un atsaukties, izmantojot šādas programmas.

- **NWChem** (bezmaksas) operētājsistēmai Windows, MAC, Linux)

## Atsauces
* [Gausa kuba faila formāts](https://paulbourke.net/dataformats/cube/)


