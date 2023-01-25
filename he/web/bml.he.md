{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ BML - קובץ שפת סימון שעועית",
  "description":"למד על פורמט קובץ BML וממשקי API שיכולים ליצור ולפתוח קובצי BML.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## מהו קובץ BML?

קובץ עם סיומת .bml הוא קובץ Bean Markup Language המאחסן מחלקות Java לתמיכה ביישומי Java. זה מאפשר גישה לאובייקטים ושיטות Java, ואינו מצריך ליצור פונקציונליות חדשה באמצעות מחלקות Java. הוא מפרט כיצד הרכיבים מחוברים זה לזה לביצוע משימות שימושיות. BML פותחה על ידי IBM alphaWorks כדי לתאר את יחסי המבנים והרכיבים. ניתן לפתוח ולהציג קבצי BML באמצעות כל עורך טקסט כגון דפדפני אינטרנט, Microsoft Notepad ו-Notepad++.

## פורמט קובץ BML

אתר IBM alphaworks סיפק שני יישומים של BML. היישום הראשון הוא מתורגמן ש'משחק' סקריפט BML ליצירת היררכיית השעועית הרצויה. המימוש השני הוא מהדר שמרכיב כל סקריפט BML לקוד Java נטול השתקפות. זה יתרון במובן זה שהוא מאפשר לכידת המבנה הבין-רכיבי של האפליקציה באמצעות שפה המיועדת למטרה ספציפית זו עם יכולת נוספת לקמפל אותו לקוד Java 'רגיל'.

## תגיות BML

להלן הסבר על חלק מהתגים המשמשים בשפת BML:

### ה<bean> תָג:

ה<bean> אלמנט משמש ליצירת שעועית חדשה או לחיפוש שעועית לפי שם. ה<bean> התג הוא בפורמט:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
ה-"id" בתג משויך לרישום האובייקטים עבור JavaBean.

### ה<string> תָג

ישנן שתי דרכים להשתמש בתג המחרוזת:

1. כדי ליצור מחרוזת לא ריקה:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. כדי ליצור מחרוזת ריקה:

```
<string/>
```
## הפניות

* [העברת הודעות מונחה עצמים עם XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [שפת הסימון הפיזית](http://web.mit.edu/mecheng/pml/standards.htm)
* [The Bean Markup Language](https://all4dev.blogspot.com/2019/06/bean-markup-language-tutorial.html)
