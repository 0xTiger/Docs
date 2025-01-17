{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ SHSH2 - פורמט קובץ SHSH Blob של iOS",
  "description":"למד על מהו קובץ SHSH2.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## מהו קובץ SHSH2?

קובץ SHSH2, הידוע גם כ-SHSH blob או ECID SHSH, הוא חתימה דיגיטלית המשמשת את אפל לאימות ואימות עדכוני קושחה עבור מכשירי iOS כגון iPhones, iPads ו-iPods. הוא מכיל מזהה ייחודי למכשיר המכונה ECID (מזהה שבב בלעדי). הוא מכיל גם מידע על גרסת הקושחה המותקנת במכשיר.

## פורמט קובץ SHSH2 - מידע נוסף

קבצי SHSH2 נשמרים בדיסק בפורמט קובץ בינארי ופרטי מבנה הקבצים הפנימיים של פורמט קובץ זה אינם זמינים לציבור.

כאשר גרסה חדשה של iOS מותקנת במכשיר Apple כגון iPhone, iPad או Mac, נוצר קובץ SHSH2. קובץ SHSH2 זה נשלח לשרתי Apple אשר קורא ומאמת את קובץ החתימה הדיגיטלית הזה. על סמך מידע זה, השרת מאפשר או מונע את ההתקנה.

אותו דבר קורה כאשר מתבקש עדכון. כאשר משתמש מבקש עדכון או שחזור של המכשיר שלו דרך iTunes או תוכנה אחרת, השרתים של אפל יבדקו שקובץ ה-SHSH2 תואם לגרסת ה-ECID והקושחה של המכשיר לפני שיאפשרו לעדכון להמשיך.

## הפניות

* [SHSH Blob - מאת ויקיפדיה](https://en.wikipedia.org/wiki/SHSH_blob)
* [חוסך TSS](https://tsssaver.1conan.com/v2/)

