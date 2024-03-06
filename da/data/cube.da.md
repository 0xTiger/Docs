{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CUBE-fil - Gaussian Cube-fil - Hvad er .cube-fil, og hvordan åbner man den?",
  "description" : "Lær om Gaussian Cube File og hvordan du åbner den.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-cube-da",
      "parent" : "data"
}
},
  "lastmod" : "2024-01-25"
}

## Hvad er en CUBE fil?

CUBE-filformat, også kendt som Gaussian Cube-fil (.cube) bruges i beregningskemi til lagring af molekylære data, især information om elektrontæthed, der stammer fra kvantekemiberegninger. Dette format er almindeligvis forbundet med **Gaussisk softwarepakke**, som er meget brugt til at udføre ab initio elektroniske strukturberegninger.

Gaussian Cube-filer gemmer tredimensionelle data, typisk repræsenterende elektrondensitet eller andre egenskaber ved molekyler, opnået gennem kvantekemiberegninger. Filen indeholder overskriftssektion med metadata (såsom oprindelse, antal datapunkter langs hver akse og afstand), efterfulgt af gitter af numeriske værdier, der repræsenterer egenskab af interesse (f.eks. elektrontæthed) ved hvert gitterpunkt i rummet.

Gaussian Cube-fil (.cube) er en almindelig tekstfil med specifik struktur. Overskriften indeholder information om molekylært system og datagitter, og dataværdier er arrangeret i tredimensionelt gitterformat. Gaussian Cube-filer bruges ofte til at visualisere molekylære egenskaber ved hjælp af molekylær visualiseringssoftware. Programmer som **VMD (Visual Molecular Dynamics)** eller **PyMOL** kan læse Gaussian Cube-filer for at vise molekylære overflader, elektrondensitet eller andre beregnede egenskaber.

## Forenklet eksempel på Gaussian Cube-fil:

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

## Om Gaussian

Gaussian er en suite af softwareapplikationer til kvantekemi og beregningskemi. Gaussians primære fokus er på ab initio kvantekemimetoder, som er meget nøjagtige, men beregningsintensive tilgange til at studere elektroniske strukturer af molekyler. Softwaren bruges i vid udstrækning i forskning og akademiske omgivelser til forskellige applikationer, herunder forudsigelse af molekylære egenskaber, undersøgelse af reaktionsmekanismer og udforskning af molekylære strukturer.

## Om NWChem

NWChem er en open source computerkemi-software designet til højtydende kvantekemi-simuleringer. Den anvender ab initio metoder såsom Hartree-Fock og densitets funktionsteori, understøtter parallel computing til effektive beregninger på klynger og finder anvendelser inden for forskellige videnskabelige områder, herunder beregningskemi, biokemi og materialevidenskab. NWChem er kendt for sin alsidighed, der giver forskere mulighed for at studere forskellige kemiske systemer, og dens open source-natur tilskynder til samfundsbidrag og tilpasning.

## Om VMD

VMD, som står for Visual Molecular Dynamics, er et kraftfuldt og udbredt molekylært visualiseringsprogram til at vise, analysere og animere molekylær dynamik (MD) baner, såvel som statiske molekylære strukturer. Det er særligt populært inden for computerkemi, molekylærbiologi og strukturel bioinformatik. VMD udmærker sig ved at visualisere molekylære strukturer ved at levere højkvalitets 3D-gengivelser af molekyler og molekylære komplekser. Det understøtter forskellige molekylære filformater.

## Om PyMOL

PyMOL er et molekylært visualiseringssystem og et softwareværktøj, der bruges til tredimensionel visualisering af molekylære strukturer. Det er særligt populært inden for områderne strukturel biologi, bioinformatik og beregningskemi. PyMOL leverer højkvalitets 3D-gengivelser af molekylære strukturer, hvilket gør det muligt for brugere at visualisere og udforske former, overflader og interaktioner af biologiske makromolekyler.

## Hvordan åbner jeg filen CUBE?

CUBE fil kan åbnes og refereres til ved hjælp af følgende programmer.

- **NWChem** (gratis) til (Windows, MAC, Linux)

## Referencer
* [Gaussian Cube File Format](https://paulbourke.net/dataformats/cube/)

