{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ HTACCESS - פורמט קובץ HTACCESS Apache",
  "description" :"מדריך פורמט הקבצים שלך כדי ללמוד מהו קובץ HTACCESS",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ HTACCESS?

קובץ HTACCESS הוא קובץ תצורה של Apache המספק מנגנון לאפשר שינויי תצורה עבור תיקיות/ספריות שונות של אתר אינטרנט. הוא כולל הנחיות תצורה החלות על הספרייה ועל ספריות המשנה.

קובץ HTACCESS מבצע מספר בדיקות כגון הגדרת עמוד האינדקס של אתר אינטרנט, פירוט דף השגיאה 404 (דף לא נמצא), ביצוע הפניות לדף 301 או 302, חסימת גישה מכתובת IP ספציפית או אתרים אחרים. השימוש בקבצי .htaccess, אפוא, מאט את הביצועים הכוללים של שרת ה-Apache [HTTP](/he/web/http/) שלך.

## פורמט קובץ HTACCESS

קבצי HTACCESS מאוחסנים בתקליטור בפורמט קובץ טקסט רגיל. זה אומר שאתה יכול לפתוח ולערוך קבצים אלה בכל עורך טקסט. אין שם לפני ה"." בקובץ .htaccess, המראה שזהו קובץ נסתר בתוך התיקיה.

## שימושים נפוצים בקובץ HTACCESS

חמישה שימושים נפוצים בקובץ HTACCESS הם כדלקמן.

### Mod_Rewrite

ניתן להשתמש בקובץ HTACCESS כדי לייעד ולשנות את אופן הצגת כתובות האתרים ודפי האינטרנט באתר למשתמשים.

### אימות

ניתן להשיג אימות עם ‎.htaccess על ידי יצירת קובץ passowrd בשם .htpasswd. זה מאפשר למבקרים באתר לספק סיסמה אם הם רוצים לבקר בחלק מסוים של דף האינטרנט.

### דפי שגיאה מותאמים אישית

אתה יכול ליצור דפי שגיאה מותאמים אישית כגון 400 בקשה שגויה, 401 נדרשת הרשאה, 403 עמוד אסור, 404 קובץ לא נמצא ו-500 שגיאה פנימית עם קובץ .htaccess. עם זאת, אלה יאטו את ביצועי השרת מכיוון שכל הבדיקות הללו יבוצעו עם הגישה לדפים.

### סוגי MIME

ניתן לשנות קבצי Apache HTACCESS כך שיכללו סוגי תוספות דואר אינטרנט רב-תכליתי (MIME). זה מאפשר לשרת שלך לתמוך במשלוח של קבצי יישומים שלא נתמכו על ידי האתר.

### SSI

Server Side Includes (SSI) פועל כחוסך זמן נהדר באתר. ניתן להפעיל את SSI על ידי הוספת הקוד הבא לקובץ ה-.htaccess שלך.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## דוגמה לקובץ Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## הפניות

* [מדריך Apache HTTP Server: קבצי .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)
