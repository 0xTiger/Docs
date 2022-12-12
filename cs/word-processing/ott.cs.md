{
  "date" : "2019-10-11",
  "keywords" :[ "soubor ott", "formát souboru ott", "co je soubor ott", "soubor", "příklad ott", "přípona souboru ott", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTT - soubor šablony OpenDocument",
  "description":"Další informace o formátu souboru OTT a rozhraních API, která mohou vytvářet a otevírat soubory OTT.",
  "linktitle" : "OTT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor OTT?

Soubory s příponou OTT představují šablonové dokumenty generované aplikacemi v souladu se standardním formátem OpenDocument OASIS. Ty jsou vytvořeny pomocí aplikací textového procesoru, jako je bezplatný OpenOffice Writer, a mohou obsahovat nastavení, která lze použít ke generování nových dokumentů z těchto souborů šablon. Tato nastavení zahrnují okraje stránky, ohraničení, záhlaví, zápatí a další nastavení stránky. Takové šablony se používají v oficiálních dokumentech, jako jsou hlavičkové papíry společností a standardizované formuláře.

## Stručná historie ##

Specifikace formátu souboru ODP jsou založeny na standardu vyvinutém jako specifikace ODF. Tyto specifikace se v minulosti vyvíjely ve formě tří verzí vyvinutých a publikovaných OASIS takto:

**2005:** Verze 1.0 byla zveřejněna v květnu 2005

**2007:** Verze 1.1 byla zveřejněna v únoru 2007

**2011:** Verze 1.2 byla zveřejněna v září 2011

Při přechodu z verzí ODF 1.0 na 1.1 došlo k poměrně malým změnám. [Verze ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) je nejnovější verzí specifikací ODF a vývojáři by ji měli konzultovat při vývoji aplikací souvisejících se čtením/zápisem ODS.

## Specifikace formátu souboru

Formát OpenDocument podporuje reprezentaci dokumentu jako jeden dokument XML a také kolekci několika dílčích dokumentů v rámci balíčku jako archiv [ZIP](/cs/Compression/ZIP/). Každý ze souborů z archivu ZIP ukládá část kompletního dokumentu. Každý vnořený dokument ukládá určitý aspekt dokumentu. Například jeden vnořený dokument obsahuje informace o stylu a jiný vnořený dokument obsahuje obsah dokumentu. Typický dokument ODF má následující součásti:

* content.xml – Obsah dokumentu a automatické styly použité v obsahu.
* styles.xml – Styly použité v obsahu dokumentu a automatické styly použité v samotných stylech.
* meta.xml – metainformace dokumentu, jako je autor nebo čas poslední akce uložení.
* settings.xml – Nastavení specifická pro aplikaci, jako je velikost okna nebo informace o tiskárně.

Kromě nich může být v balíčku mnoho dalších vnořených dokumentů, jako jsou miniatury dokumentu, obrázky atd. Soubory dokumentů jsou podmnožinou souborů ODF, kde je obsah (listy) uložen v subdokumentu //content.xml//.

## Reference ##

* [OpenDocument – z Wikipedie](https://en.wikipedia.org/wiki/OpenDocument)
