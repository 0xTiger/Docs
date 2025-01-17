{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ odp", "פורמט קובץ odp", "מהו קובץ odp", "קובץ", "דוגמה ל-odp", "סיומת קובץ odp","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - OpenOffice Presentation File Format",
  "description":"למד על פורמט קובץ ODP וממשקי API שיכולים ליצור ולפתוח קובצי ODP.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ ODP?

קבצים עם סיומת .odp מייצגים פורמט קובץ מצגת המשמש את OpenOffice.org בתקן OASISOpen. קובץ מצגת הוא אוסף שקופיות שבו כל שקופית יכולה להכיל טקסט, תמונות, עיצוב, אנימציות ומדיה אחרת. שקופיות אלו מוצגות לקהל בצורה של מצגות עם הגדרות מצגת מותאמות אישית. ניתן לפתוח קבצי ODP על ידי יישומים התואמים את פורמט OpenDocument (כגון OpenOffice או StarOffice).

## היסטוריה קצרה

מפרטי פורמט קובץ ODP מבוססים על התקן שפותח כמפרטי ODF. מפרטים אלה התפתחו בעבר בצורה של שלוש גרסאות שפותחו ופורסמו על ידי OASIS כדלקמן:

`2005` - גרסה 1.0 פורסמה במאי 2005
`2007` - גרסה 1.1 פורסמה בפברואר 2007
`2011` - גרסה 1.2 פורסמה בספטמבר 2011

היו שינויים די מינוריים במעבר מגרסאות ODF 1.0 ל-1.1. [גרסת ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) היא הגרסה העדכנית ביותר למפרטי ODF וצריך להיוועץ בה מפתחים לפיתוח יישומים הקשורים לקריאה/כתיבה של ODS.

## מפרטי פורמט קובץ

פורמט OpenDocument תומך בייצוג מסמכים כמסמך XML בודד וכן באוסף של מספר מסמכי משנה בתוך חבילה כארכיון [ZIP](/compression/zip/). כל אחד מהקבצים מארכיון ה-ZIP מאחסן חלק מהמסמך המלא. כל מסמך משנה מאחסן היבט מסוים של המסמך. לדוגמה, מסמך משנה אחד מכיל את מידע הסגנון ומסמך משנה אחר מכיל את תוכן המסמך. מסמך ODF טיפוסי כולל את הרכיבים הבאים:

* `content.xml` – תוכן מסמך וסגנונות אוטומטיים המשמשים בתוכן.
* `styles.xml` – סגנונות המשמשים בתוכן המסמך וסגנונות אוטומטיים המשמשים בסגנונות עצמם.
* `meta.xml` – מטא מידע על מסמך, כגון המחבר או שעת פעולת השמירה האחרונה.
* `settings.xml` – הגדרות ספציפיות ליישום, כגון גודל החלון או מידע המדפסת.

מלבד אלה, בחבילה יכולים להיות מסמכי משנה רבים אחרים כמו תמונה ממוזערת של מסמכים, תמונות וכו'.

קובצי מסמכים של גיליונות אלקטרוניים הם קבוצת המשנה של קובצי ODF שבהם התוכן (הגליונות) מאוחסן בתת-מסמך content.xml.

## הפניות

* [OpenDocument - מאת ויקיפדיה](https://en.wikipedia.org/wiki/OpenDocument)

