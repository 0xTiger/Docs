{
  "date": "2021-03-08",
  "keywords": [
"PML",
"ríomhléitheoir",
"síneadh",
"formáid",
"ríomhleabhar",
"Teanga Palm Markup"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid PML, Palm Markup Language agus APIs ar féidir leo comhaid PML a chruthú agus a oscailt.",
  "title": "PML - Comhad Teanga Palm Markup",
  "linktitle": "PML",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-pm-gal"
}
},
  "lastmod": "2021-03-08"
}

## Cad is comhad PML ann?

Thug Palm Inc isteach an fhormáid comhaid PML a sheasann do Palm Markup Language File. Is é an cuspóir atá aige ná doiciméid a chruthú le haghaidh eReader ar gléas léitheoireachta ríomhleabhair é atá cosúil leis an ríomhaire táibléid. Tugann an comhad PML an leagan amach do chomhad [PDB](/programming/pdb/) (ina bhfuil comhaid sonraí éagsúla) le taispeáint ar Ghléas Pailme.

## Sonraí teicniúla Comhaid PML

Is éard atá i struchtúr na gcomhad PML ná clibeanna chun socrú ríomhleabhar a chruthú, lena n-áirítear ailt, ceannteidil, eangú, agus tagairtí. Ceadaíonn sé freisin na clibeanna formáidithe ar nós Trom, caipíní Beaga, agus Forscript. Is féidir le forbróirí íomhánna a chur leis na ríomhleabhair freisin.

### Teanga Mharcála Pailme
Sonraíonn an tábla seo a leanas na horduithe PML:

|Ordú|Cur Síos|
---|---|
| \p | Leathanach nua |
| \x | Caibidil nua; is cúis le briseadh leathanach nua freisin. Cuir teideal na caibidle (agus aon chóid stíle) le \x agus \x |
| \Xn | Caibidil nua, n leibhéil eangaithe (n idir 0 agus 4 san áireamh) i dialóg na Caibidle; ní cúis le briseadh leathanaigh. Cuir teideal na caibidle (agus aon chóid stíle) le \Xn agus \Xn |
| \Cn=Teideal na caibidle | Cuir Teideal na Caibidle isteach sa liosta caibidil, le leibhéal n (cosúil le \Xn). Ní thaispeántar an téacs ar an leathanach agus ní chuireann sé iachall ar bhriseadh leathanach. D’fhéadfadh sé seo a bheith úsáideach uaireanta chun marc caibidle a chur isteach ag tús réamhrá na caibidle, mar shampla. |
| \c | Lár an bloc seo de théacs; gar le \c ar thús na líne |
| \r | Ceart údar bloc téacs; gar le \r ar thús na líne |
| \i | bloc iodálach; dún le \i |
| \u | Cuir líne faoi bhloc; dhúnadh le \u |
| \o | Bloc Overstrike; gar le \o |
| \v | Téacs dofheicthe; gar le \v (is féidir é a úsáid le haghaidh tuairimí) |
| \t | Bloc fleasc. Tosaigh ag tús líne, gar le \ t ag deireadh líne |
| \T=50% | Indents an céatadán sonraithe de leithead an scáileáin, 50% sa chás seo. Má tá an suíomh líníochta reatha thart ar an suíomh scáileáin sonraithe cheana féin, déantar neamhaird den chlib seo. |
| \w=50% | Leabú riail chothrománach de leithead céatadáin tugtha ar an scáileán, sa chás seo 50%. Cruthaíonn an chlib seo briseadh líne roimh agus ina dhiaidh. Tá an riail dírithe. Tá an comhartha faoin gcéad éigeantach. |
| \n | Athraigh go dtí an cló gnáth, atá sonraithe ag an úsáideoir |
| \s | Athraigh go stdFont; dún le \s chun filleadh ar an ngnáthchló |
| \b | Athraigh go cló trom; dún le \b chun dul ar ais go dtí an gnáthchló (neamhcheadaithe; úsáid \B ina ionad sin) |
| \l | Athraigh go Cló Mór; dún le \l chun filleadh ar an ngnáthchló |
| \B | Marcáil an téacs mar throm. Murab ionann agus an chlib \b, ní athraíonn \B an cló, mar sin is féidir téacs mór trom a bheith agat. Ní féidir \b agus \B a mheascadh sa chomhad PML céanna. |
| \Sp | Marcáil an téacs mar fhorscript. Níor chóir é a mheascadh le stíleanna eile cosúil le trom, iodálach, etc. Cuir téacs forscripte faoi iamh le \Sp. |
| \Sb | Marcáil an téacs mar shíntiús. Níor cheart é a mheascadh le stíleanna eile cosúil le trom, iodálach, srl. Cuir téacs suibscríofa isteach le \Sb. |
| \k | Déan caipíní beaga ar an téacs faoi iamh; dhúnadh le \k. Aon charachtair atá faoi iamh i gclibeanna \k (lena n-áirítear iad siúd a bhfuil variant orthu) déantar iad i gcás uachtair agus rindreáiltear iad ag pointe níos lú ná an gnáthcharachtar cás uachtair. |
| \\ | Is ionann é agus cúlslais amháin |
| \aXXX | Cuir isteach carachtar neamh-ASCII arb é deachúil XXX a chód Windows-1252. Féach ar an tábla carachtair PML le haghaidh sonraí. |
| \UXXXX | Cuir isteach carachtar neamh-ASCII a bhfuil a gcód Unicode heicsidheachúlach XXXX. Féach ar an tábla carachtair PML Breisithe le haghaidh sonraí. |
| \m=imagename.png | Cuir isteach an íomhá ainmnithe. Féach an rannán ar Íomhánna thíos. |
| \q=#linkanchorTéacs éigin\q | Déan tagairt d'ancaire naisc atá ag láthair eile sa doiciméad. Leagtar béim ar an téad tar éis an tsonraíocht ancaire agus roimh an rianáil \q nó taispeántar gur nasc í agus an doiciméad á bhreathnú. |
| \Q=linkanchor | Sonraigh nasc ancaire sa doiciméad. |
| \- | Cuir isteach fleiscín bog. Ní thaispeántar fleiscín bog ach amháin má tá sé riachtanach focal a bhriseadh trasna líne. |
| \Fn=fonóta11\Fn | Nasc an 1 le fonóta a bhfuil fonóta1 mar ainm air, agus é clibáilte ag deireadh an doiciméid PML. Féach an rannán ar Fonótaí agus Taobhbharraí thíos. |
| \Sd= barra taobh1 Barra Taoibh\Sd | Nasc an téacs Sidebar le barra taoibh a bhfuil an barra taoibh1 mar ainm air, agus é clibáilte ag deireadh an doiciméid PML. Féach an rannán ar Fonótaí agus Taobhbharraí thíos. |
| \I | Marcáil mar mhír innéacs tagartha. Cuir mír innéacs (agus aon chóid stíle) le \I agus \I.|
 

## Tagairtí

* [Teanga Palm Markup - Le MobileRead](https://wiki.mobileread.com/wiki/EReader)

* [Ríomhléitheoir - Le MobileRead](https://en.wikipedia.org/wiki/E-reader)


