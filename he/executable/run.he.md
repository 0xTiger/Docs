{
  "date" : "2023-01-31",
  "keywords" :["הפעל קובץ", "מהו קובץ הפעלה", "קובץ", "כיצד לפתוח קובץ הפעלה", "הפעל סיומת קובץ","הרחבה"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ RUN וממשקי API שיכולים ליצור ולפתוח קובצי RUN.",
  "title" :"פורמט קובץ הפעלה - קובץ הפעלה של לינוקס",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## מהו קובץ RUN?

פורמט הקובץ .run משמש בדרך כלל להפצת תוכנות או מתקיני יישומים בסביבת לינוקס. כדי להתקין את התוכנה, תצטרך להפוך את הקובץ לניתן להרצה, דבר שניתן לעשות באמצעות הפקודה הבאה:

```bash
chmod +x file_name.run 
```

לאחר מכן, תוכל להפעיל את הקובץ באמצעות הפקודה הבאה:

```bash
./file_name.run 
```

תהליך ההתקנה עשוי להשתנות בהתאם לקובץ ולתוכנית הספציפיים שאתה מנסה להתקין.

פורמט הקובץ .run הוא סוג של סקריפט מעטפת המשמש להפצת מתקיני תוכנה או יישומים בסביבת לינוקס. זוהי חבילה עצמאית הכוללת את כל הדרוש להתקנת התוכנה, כולל קבצים בינאריים, ספריות וקבצי תצורה.

חשוב לציין שקובצי .run יכולים להכיל גם קוד זדוני, ולכן תמיד כדאי לאמת את מקור הקובץ ולסרוק אותו לאיתור וירוסים לפני הפעלתו.

בנוסף, קבצי .run מסוימים עשויים לדרוש הרשאות בסיס כדי להפעיל ולהתקין, כך שייתכן שתצטרך להשתמש בפקודה "sudo" כדי להפעיל את הקובץ עם הרשאות גבוהות:

```bash
sudo ./filename.run
```

## איך פותחים קובץ RUN?

כדי לפתוח קובץ .run, עליך להפוך אותו לבר-הפעלה, דבר שניתן לעשות עם הפקודה "chmod":

```bash
chmod +x filename.run 
```

לאחר שהקובץ נעשה בר הפעלה, אתה יכול להפעיל אותו על ידי הקלדה:

```bash
./filename.run
```

הפעלת קובץ .run אינה זהה לפתיחתו בעורך טקסט. הפעלת קובץ .run תבצע את ההוראות שלו, שיכולות להיות כל דבר מהתקנת תוכנית ועד הפעלת סקריפט. כדי להציג את התוכן של קובץ .run, עליך לפתוח אותו בעורך טקסט, כגון nano או vim:

```
nano filename.run
```
אוֹ
```
vim filename.run
```

## הפניות
* [כיצד להפעיל קבצי .bin ו-.run באובונטו](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


