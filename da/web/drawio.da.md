{
  "date": "2019-10-11",
  "keywords": [
"drawio",
"drawio fil",
"drawio filformat",
"drawio filtype",
"fil",
"type",
"hvad er en drawio fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DRAWIO - Diagram.net Diagram filformat",
  "description": "Lær om DRAWIO-filformat og API'er til at oprette og åbne DRAWIO-filer.",
  "linktitle": "DRAWIO",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-drawi-dao"
}
},
  "lastmod": "2021-05-16"
}

## Hvad er en DRAWIO fil?

En fil med filtypenavnet .drawio er en tegnefil oprettet med [diagrams.net](https://www.diagrams.net/)'s draw.io, som er et open source-program til at arbejde med diagrammer. Den indeholder overordnet information om indholdet og formateringen af diagramelementerne såsom tekst, billeder, layout, former og positionering. Diagrammer understøttet af DRAWIO omfatter flowcharts, organisationsdiagrammer, kort, tekniske elementer, procesdiagrammer, diagrammer og mere. DRAWIO-filer kan eksporteres til flere forskellige formater såsom [JPG](/image/jpeg/), [PNG](/image/png/), [BMP](/image/bmp/), [XML](/web/xml/), PDF, [HTML](/web/html/) og [VSDX](/visio/vsdx/).

## DRAWIO filformat

DRAWIO-filer er vektorbilledfiler, gemt i standard XML-filformat. Udviklet af diagrams.net giver det mulighed for at gemme diagramoplysninger svarende til Microsoft Visio. DrawIO er tilgængelig som [online app](https://app.diagrams.net/) til at oprette, åbne og eksportere diagrammer til forskellige formater. Appen er baseret på mxGraph-diagrambiblioteket, der giver interaktive graf- og diagramprogrammer, der kører i enhver større browser som Chrome, Firefox, Edge og Safari.

### DRAWIO eksempel

Følgende eksempel er et simpelt rutediagram oprettet med DRAWIO-appen.

{{< figure src="../DRAWIO.png" alt="DRAWIO filformat" height="421" width="291">}}

Udgangs-XML, der genereres med eksporten, er som vist nedenfor.

```
<?xml version="1.0" encoding="UTF-8"?>
<mxfile host="app.diagrams.net" modified="2021-05-17T17:18:48.774Z" agent="5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.93 Safari/537.36" etag="jyk4LjRpkp5MiVdB0UgM" version="14.6.13" type="device">
  <diagram name="Page-1" id="74e2e168-ea6b-b213-b513-2b3c1d86103e">
    <mxGraphModel dx="946" dy="469" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1" pageWidth="1100" pageHeight="850" background="#ffffff" math="0" shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        <mxCell id="IQM8xkm7UoOLgGwT3--F-3" value="" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;" edge="1" parent="1" source="IQM8xkm7UoOLgGwT3--F-1" target="IQM8xkm7UoOLgGwT3--F-2">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-1" value="Jogging Start" style="rounded=0;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="440" y="240" width="120" height="60" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-5" value="" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;" edge="1" parent="1" source="IQM8xkm7UoOLgGwT3--F-2" target="IQM8xkm7UoOLgGwT3--F-4">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-7" value="" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;" edge="1" parent="1" source="IQM8xkm7UoOLgGwT3--F-2" target="IQM8xkm7UoOLgGwT3--F-6">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-2" value="Should Run?" style="rhombus;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="460" y="340" width="80" height="80" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-4" value="Process End" style="rounded=0;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="610" y="350" width="120" height="60" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-9" value="" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;" edge="1" parent="1" source="IQM8xkm7UoOLgGwT3--F-6" target="IQM8xkm7UoOLgGwT3--F-8">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-6" value="Run 10 KM" style="rounded=0;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="440" y="460" width="120" height="60" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-8" value="End Run" style="whiteSpace=wrap;html=1;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="440" y="600" width="120" height="60" as="geometry" />
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>

```

## Referencer ##

* [DRAWIO - Github](https://github.com/jgraph/drawio)

* [DRAWIO - Online-app](https://app.diagrams.net/)

* [Diagrams.Net](https://www.diagrams.net/)


