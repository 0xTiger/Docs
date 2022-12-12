{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "קובץ", "הרחבה", "פורמט", "פורמט קובץ 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ PLY וממשקי API שיכולים ליצור ולפתוח קובצי PLY.",
  "title" :"PLY - Polygon 3D File Format",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ PLY?

PLY, Polygon File Format, מייצג פורמט קובץ תלת מימדי המאחסן אובייקטים גרפיים המתוארים כאוסף של מצולעים. מטרת פורמט קובץ זה הייתה ליצור סוג קובץ פשוט וקל שהוא כללי מספיק כדי להיות שימושי עבור מגוון רחב של דגמים. פורמט קובץ PLY מגיע בפורמט ASCII כמו גם בפורמט בינארי לאחסון קומפקטי ולשמירה וטעינה מהירה. פורמט הקובץ משמש יישומים שונים המספקים תמיכה בקריאת קבצים בתלת מימד.

אובייקטים בפורמט PLY מתוארים על ידי אוסף של קודקודים, פרצופים ואלמנטים אחרים, יחד עם מאפיינים כגון צבע וכיוון רגיל שניתן לחבר לאלמנטים אלו. מאפיינים אחרים שניתן גם לאחסן עם האובייקט כוללים:

* נורמלי פני השטח
* קואורדינטות מרקם
*שקיפות
* ביטחון נתוני טווח
* מאפיינים עבור החלק הקדמי והאחורי של מצולע

אובייקט המיוצג על ידי פורמט PLY יכול להיות תוצאה של מקורות שונים כגון אובייקטים דיגיטליים ביד, אובייקטים מצולעים מיישומי מידול, נתוני טווח, משולשים מקוביות צועדות, נתוני שטח ומודלים של רדיוסיטי.

## היסטוריה קצרה

פורמט ה-PLY פותח בשנות התשעים על ידי גרג טורק ואחרים במעבדת הגרפיקה של סטנפורד וזו הסיבה שהוא ידוע גם כפורמט המשולש של סטנפורד. לפורמט הקובץ יש גרסה 1.0 מאז ולא בוצעו שינויים נוספים.

## פורמט קובץ PLY

אובייקט PLY פשוט מורכב מאוסף של אלמנטים לייצוג האובייקט. הוא מורכב מרשימה של (x,y,z) שלשות של קודקודים ורשימת פרצופים שהם למעשה מדדים לרשימת הקודקודים. קודקודים ופנים הם שתי דוגמאות לאלמנטים ורוב קובץ ה-PLY מורכב משני האלמנטים הללו. ניתן גם ליצור ולהצמיד מאפיינים חדשים לאלמנטים של אובייקט, אך יש להוסיף אותם בצורה כזו שתוכנות ישנות לא יישברו כאשר נתקלים במאפיינים חדשים אלו. ניתן להשליך מאפיינים כאלה גם על ידי קריאת יישומים. יתרה מכך, ניתן ליצור אלמנטים חדשים ולהגדיר מאפיינים גם עם אלמנט זה.

### מבנה הקובץ

מבנה הקובץ של פורמט קובץ PLY הוא כדלקמן:

|שדה
---|
|כותרת הקובץ
|רשימת קודקודים
|רשימת פנים
|רשימת אלמנטים נוספים

#### מבנה לדוגמה

נשתמש בדוגמה הבאה למטה בדיון הבא שלנו עבור חלקים שונים של פורמט קובץ PLY.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### כותרת הקובץ

כותרת פורמט הקובץ PLY מורכבת מטקסט ASCII הן עבור ה-ASCII והן עבור הפורמט הבינארי. קטע ההתחלה והסוף של הכותרת מזוהה על ידי מילות מפתח של רובד וכותרות סיום. בתחילת הכותרת יש את מילת הקסם ply המשמשת לזיהוי פורמט קובץ PLY על ידי הקוראים. השורה הבאה מציגה את מספר הגרסה של קובץ זה. הערות בפורמט קובץ PLY מתחילות עם מילת מפתח הערה בתחילת כל שורת הערה.

#### מילת מפתח של אלמנט

מילת המפתח של האלמנט מספרת מה יש בתוך הקובץ. אחריו מאפיינים עבור סוג האלמנט הספציפי שבו לכל מאפיין יש את סוג המאפיין והסדר שלו כפי שמוצג להלן:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

בדוגמה הספציפית הזו, לאלמנט הקודקוד הספציפי יש 3 מאפיינים מסוג float עם הסדר שצוין.

#### סוגי סוגי נתונים

ישנם שני סוגים של סוגי נתונים שיכולים להיות לנכס.

'Scalar': סוגי הנתונים הסקלאריים הם כפי שמוצג להלן:

|#שם|#סוג|#מספר בתים
|char|character|1
|uchar|תו לא חתום|1
|קצר|מספר שלם קצר|2
|short|מספר שלם קצר ללא סימן|2
|int|מספר שלם|4
|uint|מספר שלם לא חתום|4
|float|ציף דיוק יחיד|4
|double|float דיוק כפול|8

`רשימה`: קיימת צורה מיוחדת של הגדרות מאפיינים המשתמשת בסוג נתוני הרשימה. דוגמה לכך היא מקובץ הקובייה למעלה:

`רשימת נכסים uchar int vertex_index`

משמעות הדבר היא שהמאפיין "vertex_index" מכיל תחילה char ללא סימן שמספר כמה אינדקסים מכיל המאפיין, ואחריו רשימה המכילה מספרים שלמים רבים כל כך. כל מספר שלם ברשימה זו באורך משתנה הוא אינדקס לקודקוד.

## הפניות ##

* [פורמט קובץ PLY](http://paulbourke.net/dataformats/ply/)
* [PLY - מאת ויקיפדיה](https://en.wikipedia.org/wiki/PLY_(file_format))
