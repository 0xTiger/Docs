{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "فایل MP - فایل MetaPost LaTeX",
  "description":"درباره فرمت فایل MP و APIهایی که می‌توانند فایل‌های MP را ایجاد و باز کنند، بیاموزید.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp-fa",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## فایل MP چیست؟

An MP file is a vector image file generated by MetaPost programming language to create pictures. Vector images created using MP file format are saved as [EPS](/page-description-language/eps/) (Encapsulated PostScript) files. In addition, MetaPost comes distributed with TeX and Metafont frameworks and MP files can be generated from within the TEX and LTX files used by these applications. MP files contain drawing statements and mathematical algorithmic drawing for rendering the output EPS file. PDFTex engine can use the created EPS to generate [PDF](/pdf/) files directly.

## فرمت فایل MP

فایل‌های MP به عنوان فایل‌های باینری روی دیسک ذخیره می‌شوند و وقتی به فرمت فایل تصویر برداری خروجی صادر می‌شوند، خروجی EPS تولید می‌کنند. نقشه های ایجاد شده با استفاده از MetaPost به صورت قالب بندی شده در اسناد فنی و نشریات مجلات ایجاد شده با LaTex گنجانده شده است.

### نمونه فایل MetaPost MP

در زیر مثالی آورده شده است که از [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost) ارجاع داده شده است، که حاوی یک فلش و حرف A درست بالای وسط فلش است.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## منابع ##

* [MetaPost توسط Wikipedia](https://en.wikipedia.org/wiki/MetaPost)

* [نمونه لاتکس متاپست توسط ویکی آموزشی برکلی](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)


