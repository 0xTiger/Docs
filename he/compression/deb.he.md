{
  "date" : "2021-04-08",
  "keywords" :[ "קובץ deb", "פורמט קובץ deb", "מהו קובץ deb", "קובץ", "דוגמה ל-deb", "סיומת קובץ deb","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Bzip Compressed Tar Archive",
  "description":"למד על פורמט קובץ DEB וממשקי API שיכולים ליצור ולפתוח קובצי DEB.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## מהו קובץ DEB?

קובץ עם סיומת .deb הוא פורמט קובץ חבילה בינארית של דביאן הזמינה להפצה של חבילות תוכנה במערכת ההפעלה לינוקס. הוא מורכב משני קובצי ארכיון [TAR](/he/compression/tar/). ה-DPKG מספק את המנגנון לקריאה והתקנה של חבילות DEB. ניתן להתקין חבילות DEB באמצעות ממשק ניהול תוכנת חבילות APT. לקבצי DEB יש סוג מדיה באינטרנט בתור `application/vnd.debian.binary-package`.

## פורמט קובץ DEB

קובץ DEB מורכב משני קובצי ארכיון [TAR](/he/compression/tar/). ארכיון אחד מכיל את מידע הבקרה ואחר מכיל את הנתונים הניתנים להתקנה.

### ארגון החבילות

קובץ DEB הוא קובץ ארכיון **ar** בעל ערך קסם של `!<arch> `. מאז דביאן 0.93, מנגנון הארכיון של קבצי DEB מכיל שלושה קבצים בסדר מסוים.

1. `Debian Binary` - היא מיועדת לסדרה של שורות, מופרדות בשורות חדשות. נכון לעכשיו, קיימת רק שורה אחת המתארת את מספר הגרסה. מספר הגרסה הנוכחית הוא 2.0.
1. `Control Archive` - הוא מכיל ארכיון control.tar שיש בו סקריפטים לתחזוקה ומטא-אינפורמציה על החבילה כגון שם החבילה, הגרסה, התלות והמתחזק.
1. `Data Archive` - זהו ארכיון tar בשם data.tar ומכיל את קבצי המדיה הניתנים להתקנה בפועל. ניתן לדחוס את הארכיון עם gz, bz2, lzma או xz, וסיומת הקובץ של ארכיון הנתונים משתנה בהתאם.

### ארכיון בקרה

ארכיון הבקרה יכול לכלול תוכן כדלקמן.

* `שליטה` - הוא מכיל תיאור קצר של החבילה וכן מידע אחר כגון התלות שלה.
* `md5sums` - הוא מכיל סכימי בדיקה MD5 של כל הקבצים בחבילה על מנת לזהות קבצים פגומים או לא שלמים.
* `confiles` - זה מפרט את הקבצים של החבילה שיש להתייחס אליהם כקבצי תצורה. קובצי תצורה אינם נמחקים במהלך עדכון אלא אם צוין.
* `preinst`, postinst, prerm ו-postrm - סקריפטים אופציונליים המופעלים לפני או אחרי התקנה או הסרה של החבילה
* `config` הוא סקריפט אופציונלי התומך במנגנון התצורה של debconf.
* `shlibs` - זוהי רשימה של תלות ספרייה משותפת.

## הפניות

* [DEB - ויקיפדיה](https://en.wikipedia.org/wiki/Deb_(file_format))
* [פורמט חבילה בינארית של דביאן](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)
