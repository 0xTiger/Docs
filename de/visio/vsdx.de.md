{
  "date" : "2019-10-11",
  "keywords" :[ "vsdx-Datei", "vsdx-Dateiformat", "was ist eine vsdx-Datei", "Datei", "vsdx-Beispiel", "vsdx-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"Erfahren Sie mehr über das VSDX-Dateiformat und APIs, die VSDX-Dateien erstellen und öffnen können.",
  "linktitle" :"VSDX",
  "menu" : {
    "docs" : {
"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine VSDX-Datei?

Dateien mit der Erweiterung .vsdx stellen das Microsoft Visio-Dateiformat dar, das ab Microsoft Office 2013 eingeführt wurde. Es wurde entwickelt, um das binäre Dateiformat [.VSD](/de/image/vsd/) zu ersetzen, das von früheren Versionen von Microsoft Visio unterstützt wird. Es wird auch von Visio Services in Microsoft SharePoint Server 2013 unterstützt und erfordert kein zwischengeschaltetes Dateiformat für die Veröffentlichung auf SharePoint Server. Visio-Dateien werden zum Erstellen von Zeichnungen verwendet, die visuelle Objekte, Flussdiagramme, UML-Diagramme, Informationsflüsse, Organigramme, Softwarediagramme, Netzwerklayouts, Datenbankmodelle, Objektzuordnungen und andere ähnliche Informationen enthalten. Mit Visio generierte Dateien können auch in verschiedene Dateiformate wie [PNG](/de/image/png/), [BMP](/de/image/bmp/), [PDF](/de/pdf/) und andere exportiert werden.

## Datei Format ##

VSDX-Dateien basieren auf den Open Packaging Conventions und XML, und Entwickler können von diesem Format profitieren, indem sie lernen, wie sie programmgesteuert mit diesen Dateien arbeiten. Das Format erbt viele der gleichen XML-Strukturen wie seine Teile aus dem Visio-XML-Zeichnungsdateiformat (.vdx). Die Interoperabilität mit Visio-Dateien wird erheblich verbessert, da Software von Drittanbietern Visio-Dateien auf Dateiformatebene manipulieren kann.

Bestimmte andere Dateitypen, die das Dateiformat von Visio 2013 umfassen, umfassen:

* .vsdm (Visio-Makro-fähiges Zeichnen)
* .vssx (Visio-Schablone)
* .vssm (Visio-Makro-aktivierte Schablone)
* .vstx (Visio-Vorlage)
* .vstm (Visio-Makro-aktivierte Vorlage)

Unter der Haube verwendet das Dateiformat von Visio 2013 ein strukturiertes Mittel, um Anwendungsdaten zusammen mit zugehörigen Ressourcen in einem Archiv wie [ZIP](/de/compression/zip/) zu speichern. Die ZIP-Datei kann mit jedem Standard-Extraktionsprogramm extrahiert werden, wenn sie auch andere Dateitypen enthält. Sie können einfach die Dateierweiterung .vsdx durch .zip in Windows Explorer ersetzen, um den Inhalt in der VSDX-Datei anzuzeigen.

Jede Visio-Datei wird als Paket bezeichnet, das andere Dateien oder Teile enthält. Ein Paketteil kann eine XML-Datei, ein Bild oder sogar eine VBA-Lösung sein. Die Teile innerhalb des Pakets können in „Dokument“- und „Beziehungs“-Teile unterteilt werden.

### Dokumentieren ###

Die Dokumentteile enthalten den eigentlichen Inhalt und die Metadaten der Visio-Datei, wie den Namen der Datei, die erste Seite und alle darin enthaltenen Shapes und sogar die Datenverbindungen für die Shapes. Bilder und Textdateien innerhalb des Pakets werden als Dokumentteile betrachtet.

### Beziehungen ###

Die Beziehungsteile einer Visio-Datei werden im Ordner „\_rels“ gespeichert und beschreiben, wie die Teile innerhalb des Pakets miteinander in Beziehung stehen. Es stellt auch die Struktur der Datei bereit. Ein eigenständiges XML-Dokument verwendet die Eltern/Kind-Beziehung von Elementen, um die Beziehung von Entitäten zueinander zu bestimmen. Ein gültiges Visio 2013-Dateiformat enthält den richtigen Satz von Teilen, und das Paket enthält die Beziehungen zwischen den Teilen.

Beziehungsteile sind XML-Dokumente, die die Beziehungen zwischen verschiedenen Dokumentteilen innerhalb des Pakets beschreiben. Sie definieren eine Zuordnung zwischen zwei Elementen: einer angegebenen Quelle (definiert durch den Namen und Speicherort der Beziehungsdatei) und einem angegebenen Zieldokumentteil. Beispielsweise werden Beziehungsteile verwendet, um zu beschreiben, welche Formmaster mit der Datei verknüpft sind, wie Seiten mit der Datei und untereinander in Beziehung stehen oder wie Bilder und Objekte mit einer bestimmten Seite in Beziehung stehen.

## Verweise ##

* [Einführung in das Visio-Dateiformat](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
