{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo pptm", "formato de arquivo pptm", "o que é um arquivo pptm", "arquivo", "exemplo pptm", "extensão de arquivo pptm", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPTM - Formato de arquivo de apresentação do PowerPoint habilitado para macro",
  "description":"Saiba mais sobre o formato de arquivo PPTM e APIs que podem criar e abrir arquivos PPTM.",
  "linktitle" : "PPTM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

Arquivos com extensão PPTM são arquivos de apresentação habilitados para macro que são criados com o Microsoft PowerPoint 2007 ou versões superiores. Eles são semelhantes aos arquivos [PPTX](/pt/presentation/pptx/) com a diferença de que os laterais não podem executar macros embora possam conter macros. Os arquivos PPTM podem ser editados abrindo-os no Microsoft PowerPoint e atualizando o conteúdo. Outro formato semelhante é o PPSM, mas é somente leitura por padrão e inicia a apresentação de slides quando aberto. O PPTM, como o PPTX, contém slides para diferentes elementos de apresentação, como texto, imagens, vídeos, gráficos e outros materiais relacionados.

## Breve história ##

O formato de arquivo PPTM foi introduzido em 2007 e usa o padrão Open XML adaptado pela Microsoft em 2000. O novo tipo de arquivo tem vantagens adicionais de tamanhos de arquivo pequenos, menos alterações de corrupção e representação de imagens bem formatadas. Foi no início de 2000, quando a Microsoft decidiu fazer a mudança para acomodar o padrão para **Office Open XML**. Em 2007, esse novo formato de arquivo passou a fazer parte do Office 2007 e é mantido também nas novas versões do Microsoft Office.

## Especificações de formato de arquivo ##

Arquivos gerados com o formato de arquivo Office Open XML é uma coleção de arquivos XML junto com outros arquivos que fornecem links entre todos os arquivos constituintes. Esta coleção é na verdade um arquivo compactado que pode ser extraído para visualizar seu conteúdo. Para isso, basta renomear a extensão do arquivo PPTM com zip e extraí-lo para observar seu conteúdo.

As seções seguintes lançam alguma luz sobre cada uma delas.

### [Content_Types].xml ###

Este é o único arquivo encontrado no nível base quando o zip é extraído. Ele lista os tipos de conteúdo para peças dentro do pacote. Todas as referências aos arquivos XML incluídos no pacote são referenciadas neste arquivo XML. A seguir está um tipo de conteúdo para uma parte do slide:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Se novas partes precisarem ser adicionadas ao pacote, isso pode ser feito adicionando a nova parte e atualizando quaisquer relacionamentos dentro dos arquivos .rels. Deve-se ter em mente que para tal mudança, o Content_Types.xml também deve ser atualizado.

### \_rels (Pasta) ###

Os relacionamentos entre as outras partes e os recursos fora do pacote são mantidos pela parte de relacionamentos. A pasta Relacionamentos contém um único arquivo XML que armazena os relacionamentos em nível de pacote. Os links para as partes principais dos arquivos de apresentação estão contidos neste arquivo como URIs. Esses URIs identificam o tipo de relacionamento de cada parte chave com o pacote. Isso inclui o relacionamento com o documento principal do escritório localizado como ppt/presentation.xml e outras partes dentro do docProps como propriedades principais e estendidas.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Cada parte do documento que é a fonte de um ou mais relacionamentos terá sua própria parte de relacionamentos onde cada parte de relacionamento é encontrada em uma subpasta \_rels da parte e é nomeada anexando '.rels' ao nome do papel. A parte de conteúdo principal (presentation.xml) tem sua própria parte de relacionamentos (presentation.xml.rels). Ele contém relacionamentos com outras partes do conteúdo, como slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, bem como os URIs para links externos.

#### Relacionamento explícito ####

Para um relacionamento explícito, um recurso é referenciado usando o atributo Id de um<Relationship> elemento. Ou seja, o Id na origem mapeia diretamente para um Id de um item de relacionamento, com uma referência explícita ao destino.

Por exemplo, um slide pode conter um hiperlink como este:
```
<a:hlinkClick r:id#"rId2">
```
O r:id#"rId2" faz referência ao seguinte relacionamento dentro da parte de relacionamentos do slide (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Relação Implícita ####

Para um relacionamento implícito, não há referência direta a um `<Relationship> ID`. Em vez disso, a referência é compreendida.

### Pasta ppt ###

Esta é a pasta principal que contém todos os detalhes sobre o conteúdo da Apresentação. Por padrão, ele possui as seguintes pastas:

* \_rels
* tema
* diapositivos
* layouts de slides
* slideMasters

e os seguintes arquivos xml:

* apresentação.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Referências ##

* [[MS-PPTX] - Formato de arquivo PPTX](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)
