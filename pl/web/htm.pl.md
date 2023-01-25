{
  "date" : "2019-10-11",
  "keywords" :[ "htm","plik htm", "format pliku htm", "typ pliku htm", "plik", "typ", "co to jest plik htm" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku HTML",
  "description" :"Twój przewodnik po formatach plików, aby dowiedzieć się, co to jest plik HTM i interfejsy API, które mogą je tworzyć i otwierać.",
  "linktitle" : "HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik HTM?

Pliki z rozszerzeniem **.htm** reprezentują Hypertext Markup Language do tworzenia stron internetowych do wyświetlania w przeglądarkach internetowych, takich jak Google Chrome, Internet Explorer, Firefox i wielu innych. Definiuje znaczniki do tworzenia statycznych stron, które mają być publikowane w sieci World Wide Web (WWW) w celu uzyskania dostępu przez inne osoby. Te znaczniki informują przeglądarki, jak wyświetlić zawartość strony internetowej. Takie strony mogą zawierać zwykły tekst, obrazy, hiperłącza do innych stron, filmy i inne informacje multimedialne. Po opublikowaniu strony internetowej możesz zobaczyć kod znaczników, który się za nią kryje, przeglądając jej źródło. Nowoczesne przeglądarki umożliwiają wgląd w każdą sekcję strony internetowej, w której opracowano każdy podpodział lub element znaczników w źródle HTM.

## Krótka historia HTM

Od momentu powstania i pierwszej roli, specyfikacje HTML są utrzymywane przez World Wide Web Consortium (W3C) od 1996 roku. W 2000 roku stały się również międzynarodowym standardem (ISO/IEC 15445:2000). W 1999 roku opublikowano HTML 4.01. W 2004 r. grupa robocza Web Hypertext Application Technology Working Group (WHATWG) rozpoczęła prace nad wersją HTML5, która stała się wspólnym produktem z W3C w 2008 r. Została ukończona i znormalizowana 28 października 2014 r.

## Format pliku HTML

Dokument HTML 4 składa się z trzech części:

1. linia zawierająca informacje o wersji HTML
1. deklaratywna sekcja nagłówka
1. treść, która zawiera rzeczywistą treść dokumentu. Treść może być zaimplementowana przez element BODY lub element FRAMESET w celu umieszczenia treści w ramkach

Każda sekcja może być wiodąca lub zakończona spacjami, znakami nowej linii, tabulatorami i komentarzami. Poniżej przedstawiono przykład prostego dokumentu HTML:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Informacje o wersji

Pierwsza linia kodu,<!DOCTYPE html> , jest nazywany deklaracją typu dokumentu i informuje przeglądarkę, w której wersji HTML napisana jest strona. W zależności od wersji HTML istnieje wiele różnych deklaracji typu dokumentu, które określają definicję typu dokumentu (DTD) używaną dla dokumentu. Każde DTD różni się od innych obsługiwanymi elementami i różni się w następujący sposób:

* HTML 4.01 Strict — obejmuje wszystkie elementy i atrybuty, które nie zostały [przestarzałe] (https://www.w3.org/TR/html401/conform.html#deprecated) lub nie pojawiają się w dokumentach zestawów ramek
* HTML 4.01 Transitional - zawiera wszystko w ścisłym DTD plus przestarzałe elementy i atrybuty (z których większość dotyczy prezentacji wizualnej
* Zestaw ramek HTML 4.01 — zawiera również wszystko w przejściowych ramkach DTD plus

W przypadku **HTML5** informacje o wersji są takie, jak podano poniżej.

```
<!DOCTYPE html>
```

### Informacje nagłówka

Nagłówek dokumentu HTML może zawierać wiele elementów HTML, które nie są renderowane przez przeglądarkę. Takie elementy to albo metadane, które opisują informacje o stronie, albo zawierają sekcje, które służą do pobierania informacji z zasobów zewnętrznych, takich jak arkusze stylów CSS lub pliki JavaScript. Nagłówek strony jest reprezentowany przez \<head> tag i kończy się na \</head> etykietka.

<html>Aby ustawić tytuł strony, \<title> jest jedynym wymaganym elementem w tagach \<head>. To samo jest używane przez wyszukiwarki do identyfikacji tytułu strony. </html>

### Informacje o ciele

Jest to główna sekcja w pliku, która zawiera całą zawartość pliku renderowaną przez przeglądarki. Treść HTML może zawierać znaczniki, które mogą odnosić się do różnych bloków konstrukcyjnych w postaci znaczników. Może zawierać kilka różnych rodzajów informacji, takich jak tekst, obrazy, kolory, grafika itp. Ponadto elementy audio i wideo mogą być również osadzone w treści HTML w celu renderowania przez przeglądarki. W obecności nowoczesnych aplikacji arkuszy stylów do reprezentacji wizualnej atrybuty prezentacji BODY, takie jak kolor tła, kolor łącza, kolor tekstu itp., zostały wycofane. W ten sposób te same efekty można osiągnąć za pomocą arkuszy stylów, jak pokazano poniżej:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Wbudowane arkusze stylów można łatwo osadzić, a do szybkich zastosowań efektów wizualnych zewnętrzne arkusze stylów ułatwiają jednorazowe wdrożenie i dostęp w wielu miejscach.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### Elementy HTML

Jak wspomniano wcześniej, treść wewnątrz treści HTML jest reprezentowana przez znaczniki, znane również jako elementy HTML. Każdy znacznik może posiadać dodatkowe informacje w postaci atrybutów, które są zapisywane jako
```
<tag attribute1#"value1" attribute2#"value2">
```
chociaż nie jest konieczne posiadanie atrybutów z każdym tagiem. Jeśli atrybuty nie są wymienione, w każdym przypadku używane są wartości domyślne. Poniżej przedstawiono niektóre przykłady Elementów:

#### Nagłówek

```
<head>
  <title>The Title</title>
</head>
```

#### Nagłówki

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### akapity

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Bibliografia

* [Globalna struktura dokumentu HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)
