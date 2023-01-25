{
  "date" : "2019-10-11",
  "keywords" :[ "fichier ott", "format de fichier ott", "qu'est-ce qu'un fichier ott", "fichier", "exemple ott", "extension de fichier ott","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTT - Fichier de modèle OpenDocument",
  "description":"En savoir plus sur le format de fichier OTT et les API qui peuvent créer et ouvrir des fichiers OTT.",
  "linktitle" : "OTT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier OTT ?

Les fichiers avec l'extension OTT représentent des modèles de documents générés par des applications conformément au format standard OpenDocument d'OASIS. Ceux-ci sont créés avec des applications de traitement de texte telles que OpenOffice Writer gratuit et peuvent contenir des paramètres pouvant être utilisés pour générer de nouveaux documents à partir de ces fichiers modèles. Ces paramètres incluent les marges de page, les bordures, les en-têtes, les pieds de page et d'autres paramètres de page. Ces modèles sont utilisés dans les documents officiels tels que les en-têtes d'entreprise et les formulaires standardisés.

## Bref historique ##

Les spécifications du format de fichier ODP sont basées sur la norme développée en tant que spécifications ODF. Ces spécifications ont évolué au cours du passé sous la forme de trois versions développées et publiées par OASIS comme suit :

**2005 :** La version 1.0 a été publiée en mai 2005

**2007 :** La version 1.1 a été publiée en février 2007

**2011 :** La version 1.2 a été publiée en septembre 2011

Il y a eu des changements assez mineurs lors de la transition des versions ODF 1.0 à 1.1. La [version ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) est la dernière version des spécifications ODF et doit être consultée par les développeurs pour le développement d'applications liées à la lecture/écriture ODS.

## Spécifications du format de fichier

Le format OpenDocument prend en charge la représentation du document en tant que document XML unique ainsi qu'une collection de plusieurs sous-documents dans un package en tant qu'archive [ZIP](/fr/Compression/ZIP/). Chacun des fichiers de l'archive ZIP stocke une partie du document complet. Chaque sous-document stocke un aspect particulier du document. Par exemple, un sous-document contient les informations de style et un autre sous-document contient le contenu du document. Un document ODF typique comprend les composants suivants :

* content.xml – Contenu du document et styles automatiques utilisés dans le contenu.
* styles.xml – Styles utilisés dans le contenu du document et styles automatiques utilisés dans les styles eux-mêmes.
* meta.xml - Documentez les méta-informations, telles que l'auteur ou l'heure de la dernière action d'enregistrement.
* settings.xml - Paramètres spécifiques à l'application, tels que la taille de la fenêtre ou les informations sur l'imprimante.

Outre ceux-ci, le package peut contenir de nombreux autres sous-documents tels que des vignettes de document, des images, etc. Les fichiers de document sont le sous-ensemble de fichiers ODF dans lequel le contenu (feuilles) est stocké dans //content.xml// subdocument.

## Références ##

* [OpenDocument - Par Wikipédia](https://en.wikipedia.org/wiki/OpenDocument)
